import matplotlib.pyplot as plt


# Function to read coordinates from a text file
def read_coordinates(coordinate_file):
    with open(coordinate_file, 'r') as file:
        lines = file.readlines()
        x_cords = [int(line.split(',')[0]) for line in lines]
        y_cords = [int(line.split(',')[1]) for line in lines]
    return {x_cords, y_cords}


# Function to plot the coordinates on a scatter plot
def plot_coordinates(x, y, color='blue'):
    plt.scatter(x, y, color=color)
    plt.xlabel('X')
    plt.ylabel('Y')
    plt.title('Original Coordinates')
    plt.show()


# Function to move (translate) the points
def translate_points(local_x_coordinates, local_y_coordinates, change_in_x, change_in_y):
    translated_x_cords = [x + change_in_x for x in local_x_coordinates]
    translate_y_cords = [y + change_in_y for y in local_y_coordinates]
    return translated_x_cords, translate_y_cords


# Read coordinates from the text file
def read_coordinates(coordinate_file):
    file_name = 'coordinate_file'
    x_coordinates, y_coordinates = read_coordinates(coordinate_file)


# Plot the original coordinates
def plot_coordinates(x, y):
    plot_coordinates(x, y)

# Plot the translated coordinates in a different color
def translate_coordinates(coordinate_file):
    plot_coordinates(translated_x, color='red')

# Move (translate) the points
def translate_points(coordinate_file):
    dx = 5
    dy = 5
    translate_points(x_coordinates, y_coordinates, dx, dy)
