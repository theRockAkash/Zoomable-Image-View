# Zoomable-Image-View

Use
```
 <com.zapp.app.utils.ZoomableImageView
        android:id="@+id/iv_zoom"
        android:layout_width="match_parent"
        android:layout_height="match_parent"
        android:contentDescription="@string/zoomable_image"
        android:src="@drawable/placeholder" />
```

Or

```
  fun showFullImage(s: String) {
        val binding = ZoomImageLayoutBinding.inflate(layoutInflater)
        val dialog = AlertDialog.Builder(this)
            .setCancelable(false)
            .setView(binding.root)
            .create()
        dialog.show()

        Glide.with(this)
            .load(s)
            .placeholder(R.drawable.loading)
            .error(R.drawable.error)
            .into(binding.ivZoom)
        binding.close.setOnClickListener {
            dialog.dismiss()
        }

    }
```
