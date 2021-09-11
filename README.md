# WarMaChain


Azure LuxJam entry
Theme : ChainReaction
GameName : WarMaChain

Technologic advancement pushes world to a war. Try and conquer the world!

Software used : 
    UnrealEngine 4.27
    VSCode
    Blender
    Adobe Photoshop
    BoscaCeoil
    SFXR



How To Play : 
    World is consisting of HexagonalTiles
    
    SetupPhase : Set your troops ? // need to figure out how and what to setup

        if(player.dead == false || player.OccupiedTiles != Map.TotalTiles)
        {

            Scientist.Develop(BOMBA);
            BOMBA.SetSelfDetonateTimer(float X seconds);

            player.BOMB(SelectedHexagonalTile); // should throw bomb to another tile before explotion!

            PrintString("You Have Abandoned Reason and Started a WorldWar. YOU ARE THE WarMaChain!");


            BombedCountry.Refuge(AdjacentHexagonalTiles.Random) // The City/Country exploded by your BOMBA refuges on NeighboringCountry

            RefugedCountry.SetConfusionTimer(float ConfSeconds)

            RefugedCountry.OnConfTimerEnd(){
               RefugedCountry.BOMB(PlayerTiles.Random);
           }

            player.Dodge(
               Occupy(EmptyHexagonalTile); 
           )    // move to another tile!

            if (player.TroopCount > 0)
            {
                player.Attack(Enemy);
                Enemy.Attack(player);
            } // need to figureout how!!!

            // looping
            Scientist.Develop(BOMBA);
            BOMBA.SetSelfDetonateTimer(float X seconds);
            player.BOMB(SelectedHexagonalTile); // hitting enemytile is adviced!
           >...

        }else if(player.dead==true){
            HandleGameEnd(bool bLose);
        }else{
            HandleGameEnd(bool bWin);
        }
    
