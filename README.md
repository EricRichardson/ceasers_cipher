def code (string, shift)
  puts "Coding message..."
  coded_string = Array.new
string.each_char do |c|
  coded_string << c.ord + shift
end
coded_string
end

def decode (coded_string, shift)
  puts "Decoding message..."
  decoded_string = String.new
coded_string.each do |c|
  decoded_string += ((c - shift).chr)
end
  decoded_string
end

puts "Enter a message to be coded"
string = gets.chomp
puts "Enter the shift value"
shift = gets.to_i
string = code(string, shift)
puts string
puts "Enter the deshift value"
deshift = gets.to_i
string = decode(string, deshift)
puts string

gets
