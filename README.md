<!---
Ken3hin/Ken3hin is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->

namespace MyeventHandler
{
    public class Class1
    {
        // Define a class for the event
        public delegate void MyEventHandler(object sender, EventArgs e);

        //define a class with the event
        public class Myclass
        {
            public event MyEventHandler MyEvent;

            public void TriggerEvent ()
            {
                if (MyEvent != null)
                {
                    MyEvent (this, EventArgs.Empty);
                }
            }
        }
        // Sublcriber Class 
        public class Subcriber
        {
            public void OnEventTriggered (object sender, EventArgs e)
            {
                OnEventTriggered (sender, e); 
            }
        }
    }

}
