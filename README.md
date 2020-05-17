# Tic-Tac-Toe-game
Tic Tac Toe  application with using android studio.

![tic](https://user-images.githubusercontent.com/64914825/82136966-0ac93780-9831-11ea-8d58-78016c04433e.jpg)


![video_2020-05-17_11-46-51](https://user-images.githubusercontent.com/64914825/82137341-b758e880-9834-11ea-95d0-959488793384.gif)




step 1:-
copy this Xml file:- 


    xmlns:app="http://schemas.android.com/apk/res-auto"
    xmlns:tools="http://schemas.android.com/tools"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    tools:context=".MainActivity">

    <TextView
        android:id="@+id/textView"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:layout_marginTop="80dp"
        android:fontFamily="cursive"
        android:includeFontPadding="false"
        android:text="@string/welcome_to_tic_tec_toe"
        android:textColor="#E101FF"
        android:textSize="40dp"
        android:textStyle="bold"
        app:layout_constraintLeft_toLeftOf="parent"
        app:layout_constraintRight_toRightOf="parent"
        app:layout_constraintTop_toTopOf="parent" />

    <ImageView
        android:id="@+id/imageView"
        android:layout_width="0dp"
        android:layout_height="0dp"
        android:contentDescription="@string/OUR_MAIN_GRID"
        app:layout_constraintBottom_toBottomOf="parent"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toBottomOf="@+id/textView"
        app:srcCompat="@drawable/grid" />

    <LinearLayout
        android:layout_width="418dp"
        android:layout_height="416dp"
        android:orientation="vertical"
        app:layout_constraintBottom_toBottomOf="@+id/imageView"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintStart_toStartOf="@+id/imageView"
        app:layout_constraintTop_toBottomOf="@+id/textView">

        <LinearLayout
            android:layout_width="match_parent"
            android:layout_height="137dp"
            android:orientation="horizontal">

            <ImageView
                android:id="@+id/imageView1"
                android:layout_width="match_parent"
                android:layout_height="match_parent"
                android:layout_weight="1"
                android:onClick="playerTap"
                android:padding="10sp"
                android:tag="0" />

            <ImageView
                android:id="@+id/imageView2"
                android:layout_width="match_parent"
                android:layout_height="match_parent"
                android:layout_weight="1"
                android:onClick="playerTap"
                android:padding="10sp"
                android:tag="1" />

            <ImageView
                android:id="@+id/imageView3"
                android:layout_width="match_parent"
                android:layout_height="match_parent"
                android:layout_weight="1"
                android:onClick="playerTap"
                android:padding="10sp"
                android:tag="2" />
        </LinearLayout>

        <LinearLayout
            android:layout_width="match_parent"
            android:layout_height="139dp"
            android:orientation="horizontal">

            <ImageView
                android:id="@+id/imageView4"
                android:layout_width="match_parent"
                android:layout_height="match_parent"
                android:layout_weight="1"
                android:onClick="playerTap"
                android:padding="10sp"
                android:tag="3" />

            <ImageView
                android:id="@+id/imageView5"
                android:layout_width="match_parent"
                android:layout_height="match_parent"
                android:layout_weight="1"
                android:onClick="playerTap"
                android:padding="10sp"
                android:tag="4" />

            <ImageView
                android:id="@+id/imageView6"
                android:layout_width="match_parent"
                android:layout_height="match_parent"
                android:layout_weight="1"
                android:onClick="playerTap"
                android:padding="10sp"
                android:tag="5" />
        </LinearLayout>

        <LinearLayout
            android:layout_width="match_parent"
            android:layout_height="140dp"
            android:orientation="horizontal">

            <ImageView
                android:id="@+id/imageView7"
                android:layout_width="match_parent"
                android:layout_height="match_parent"
                android:layout_weight="1"
                android:onClick="playerTap"
                android:padding="10sp"
                android:tag="6" />

            <ImageView
                android:id="@+id/imageView8"
                android:layout_width="match_parent"
                android:layout_height="match_parent"
                android:layout_weight="1"
                android:onClick="playerTap"
                android:padding="10sp"
                android:tag="7" />

            <ImageView
                android:id="@+id/imageView9"
                android:layout_width="match_parent"
                android:layout_height="match_parent"
                android:layout_weight="1"
                android:onClick="playerTap"
                android:padding="10sp"
                android:tag="8" />
        </LinearLayout>

    </LinearLayout>

    <TextView
        android:id="@+id/status"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:layout_marginBottom="20dp"
        android:text="X's turn - Tap to play"
        android:textSize="24sp"
        android:textStyle="bold|italic"
        app:layout_constraintBottom_toBottomOf="@+id/imageView"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintStart_toStartOf="parent" />

</androidx.constraintlayout.widget.ConstraintLayout>

>


step 2:- 

    import files
    import android.os.Bundle;
    import android.view.View;
    import android.widget.ImageView;
    import android.widget.TextView;


step 3:-
create new object

        public void gameReset(View view){
        gameActive =true;
        activePlayer =0;
        for(int i=0; i<=gameState.length;i++){
            gameState[i] = 2;
        }
        ((ImageView)findViewById(R.id.imageView1)).setImageResource(0);
        ((ImageView)findViewById(R.id.imageView2)).setImageResource(0);
        ((ImageView)findViewById(R.id.imageView3)).setImageResource(0);
        ((ImageView)findViewById(R.id.imageView4)).setImageResource(0);
        ((ImageView)findViewById(R.id.imageView5)).setImageResource(0);
        ((ImageView)findViewById(R.id.imageView6)).setImageResource(0);
        ((ImageView)findViewById(R.id.imageView7)).setImageResource(0);
        ((ImageView)findViewById(R.id.imageView8)).setImageResource(0);
        ((ImageView)findViewById(R.id.imageView9)).setImageResource(0);
        TextView status = findViewById(R.id.status);
        status.setText("X's turn - Tap to play");
    }

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);
    }
}

step 4:- 
copy in user Activity

            ImageView img = (ImageView) view;
            int tappedImage = Integer.parseInt(img.getTag().toString());
            if(!gameActive){
            gameReset(view);
            }
            if(gameState[tappedImage] == 2 ){
            gameState[tappedImage] = activePlayer;
            img.setTranslationY(-1000f);
            if(activePlayer == 0){
                img.setImageResource(R.drawable.x);
                activePlayer = 1;
                TextView status = findViewById(R.id.status);
                status.setText("O's turn - Tap to play");
            }
            else {
                img.setImageResource(R.drawable.o);
                activePlayer = 0;
                TextView status = findViewById(R.id.status);
                status.setText("X's turn - Tap to play");
            }
            img.animate().translationYBy(1000f).setDuration(300);
            }
            // check if any player won
            for (int[] winPosition : winPositions){
            String Result;
            if(gameState[winPosition[0]] == gameState[winPosition[1]] &&
                    gameState[winPosition[1]] == gameState[winPosition[2]] &&
                    gameState[winPosition[0]] != 2 ) {

                gameActive = false;
                if(gameState[winPosition[0]] == 0) {
                    Result = "X has WON"; TextView status = findViewById(R.id.status);
                    status.setText(Result);

                }
                else if (gameState[winPosition[0]] == 1){
                    Result = "O has WON";
                    TextView status = findViewById(R.id.status);
                    status.setText(Result);

                }
                else {
                    Result = "Match is draw";
                    TextView status = findViewById(R.id.status);
                    status.setText(Result);
                }

                //Update the result

                }


full code:-

    public class MainActivity extends AppCompatActivity {
    boolean gameActive = true;
    // player representation
    // 0 - X
    // 1 - O

    int activePlayer = 0;
    int[] gameState = { 2, 2, 2, 2, 2, 2, 2, 2, 2};
    //  State Meanings:-
    //  0 - X
    //  1 - O
    //  2 - Null
    int[][] winPositions = {{0,1,2}, {3,4,5}, {6,7,8},
                            {0,3,6}, {1,4,7}, {2,5,8},
                            {0,4,8}, {2,4,6}};
    public void playerTap(View view){
        ImageView img = (ImageView) view;
        int tappedImage = Integer.parseInt(img.getTag().toString());
        if(!gameActive){
            gameReset(view);
        }
        if(gameState[tappedImage] == 2 ){
            gameState[tappedImage] = activePlayer;
            img.setTranslationY(-1000f);
            if(activePlayer == 0){
                img.setImageResource(R.drawable.x);
                activePlayer = 1;
                TextView status = findViewById(R.id.status);
                status.setText("O's turn - Tap to play");
            }
            else {
                img.setImageResource(R.drawable.o);
                activePlayer = 0;
                TextView status = findViewById(R.id.status);
                status.setText("X's turn - Tap to play");
            }
            img.animate().translationYBy(1000f).setDuration(300);
        }
        // check if any player won
        for (int[] winPosition : winPositions){
            String Result;
            if(gameState[winPosition[0]] == gameState[winPosition[1]] &&
                    gameState[winPosition[1]] == gameState[winPosition[2]] &&
                    gameState[winPosition[0]] != 2 ) {

                gameActive = false;
                if(gameState[winPosition[0]] == 0) {
                    Result = "X has WON"; TextView status = findViewById(R.id.status);
                    status.setText(Result);

                }
                else if (gameState[winPosition[0]] == 1){
                    Result = "O has WON";
                    TextView status = findViewById(R.id.status);
                    status.setText(Result);

                }
                else {
                    Result = "Match is draw";
                    TextView status = findViewById(R.id.status);
                    status.setText(Result);
                }

                //Update the result

            }

        }


    }
    public void gameReset(View view){
        gameActive =true;
        activePlayer =0;
        for(int i=0; i<=gameState.length;i++){
            gameState[i] = 2;
        }
        ((ImageView)findViewById(R.id.imageView1)).setImageResource(0);
        ((ImageView)findViewById(R.id.imageView2)).setImageResource(0);
        ((ImageView)findViewById(R.id.imageView3)).setImageResource(0);
        ((ImageView)findViewById(R.id.imageView4)).setImageResource(0);
        ((ImageView)findViewById(R.id.imageView5)).setImageResource(0);
        ((ImageView)findViewById(R.id.imageView6)).setImageResource(0);
        ((ImageView)findViewById(R.id.imageView7)).setImageResource(0);
        ((ImageView)findViewById(R.id.imageView8)).setImageResource(0);
        ((ImageView)findViewById(R.id.imageView9)).setImageResource(0);
        TextView status = findViewById(R.id.status);
        status.setText("X's turn - Tap to play");
    }

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);
    }
    }

