# message-to-matrix

This Custom Action allows you to send a message to a matrix room.


## Usage

```
message-to-matrix:
  name: Matrix notification
  if: always()
  runs-on: ubuntu-latest
  needs: calendario_negrita
  steps:
    - name: Create calendar month
      uses: NeddM/message-to-matrix@main
      with:
        token: ${{ secrets.MATRIX_TOKEN }}
        room_id: ${{ secrets.MATRIX_ROOM_ID }}
        message: "Hello World!"
        base_url: "https://matrix-client.matrix.org"
```

