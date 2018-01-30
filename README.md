# MovableFloatingActionButton
A Movable FAB that is keeped on layout border

On OnCreate method, call setCoordinatorLayout like this:

 @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.main_activity);

        MovableFloatingActionButton fab = (MovableFloatingActionButton) findViewById(R.id.fab);
        CoordinatorLayout.LayoutParams lp  = (CoordinatorLayout.LayoutParams) fab.getLayoutParams();
        fab.setCoordinatorLayout(lp);
        }

On xml layout, use it like this:

//set the filepath where MovableFAB is in

<com.filepath.MovableFloatingActionButton
        android:id="@+id/fab"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:layout_alignParentStart="true"
        android:layout_alignParentTop="true"
        android:layout_gravity="bottom|end"
        android:layout_marginBottom="@dimen/fab_margin"
        android:layout_marginEnd="@dimen/fab_margin"
        android:src="@drawable/ic_fab_icon"
        app:fabSize="normal"
        app:layout_anchorGravity="bottom|right|end" />
