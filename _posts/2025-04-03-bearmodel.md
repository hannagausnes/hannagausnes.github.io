# Classifying Bears with FastAI 🐻

In one of our lectures we built an image classifier that can recognize and tell the difference between grizzly bears, black bears, and... teddy bears.

🧪 The Goal: Train a deep learning model to accurately classify images into one of three categories:
- grizzly
- black
- teddy

🛠️ How We Did It: FastAI makes this super beginner-friendly. Here’s what we did:
- Used fastdownload and fastai.vision.all to load everything we needed.
- We built a DataLoaders object from a folder structure with images of the three bear types.

📈 Results: After training, I evaluated the model on a few test images. It correctly classified photos like:
- A big brown bear in the wild → Grizzly
- A small bear with shiny black fur → Black
- A fuzzy teddy sitting on a bed → Teddy

🧑‍🎓 Things I Learned
One really interesting challenge we ran into was that images come in all shapes and sizes. That’s a problem for models which expect inputs to have the same dimensions. So what do you do?
- Crop the images? You might lose important parts of the picture.
- Resize (squish) them? That keeps everything but messes up the proportions.

We ended up using random resized crop, which is a nice compromise. It crops a random part of the image and resizes it to a standard size, helping the model learn to focus on different areas while keeping training more consistent.
This acts like a kind of data augmentation—it makes the model more robust since it learns from slightly different views of the same object.
