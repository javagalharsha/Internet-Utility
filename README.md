# Internet-Utility

 Getting Started with Internet Utility: 

 The Internet utility class gives information about the internet connection. 

Usage:

For checking internet connection -
		
		InternetUtility.isConnected(getApplicationContext();

	It returns true if internet is connected else returns false




To get connection type -

		InternetUtility.getConnectionType(getApplicationContext();

	It returns a byte value. Compare this value with the static variable of InternetUtility class to know the connection type as follows.

To check the change in connection type during runtime - 

	implement the ConnectionTypeChangeListener interface

		public class SampleActivity extends AppCompatActivity implements

		InternetUtility.ConnectionTypeChangeListener {

	initialize the listener by passing interval time for timer

		new InternetUtility().

		setConnectionTypeChangeListener(this,getApplicationContext(),0,5000);


	override onConnectionTypeChanged() method where it will return the new connection type
	when it changed.

		@Override
		public void onConnectionTypeChanged(byte type) { 

		}
