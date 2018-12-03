# javascript-bootbox-pupover

1.http://bootboxjs.com



=================================================================================
$(document).on("click", ".MyLink", function (e) {
    var link = $(this).attr("href"); // "get" the intended link in a var
    e.preventDefault();

    bootbox.confirm({
        message: "Xác nhận xóa bản ghi?",
        buttons: {
            confirm: {
                label: 'Đồng ý',
                className: 'btn-danger'
            },
            cancel: {
                label: 'Hủy bỏ',
                className: 'btn-default'
            }
        },
        callback: function (result) {
            if (result) {
                document.location.href = link;
            }
        }
    });
});
