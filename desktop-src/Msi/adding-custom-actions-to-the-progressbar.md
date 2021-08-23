---
description: Les actions personnalisées peuvent ajouter des informations de temps et de progression à un contrôle ProgressBar. Pour plus d’informations sur la création d’une boîte de dialogue d’affichage des actions avec un ProgressBar, consultez Création d’un contrôle ProgressBar.
ms.assetid: 101e6b59-3791-450c-9dc6-8930bd665a93
title: Ajout d’actions personnalisées au ProgressBar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d83dfeb806eb0ed6f1e251dd48b97911d8e0f583c8b65cb48ef0d04df059ebb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119811059"
---
# <a name="adding-custom-actions-to-the-progressbar"></a>Ajout d’actions personnalisées au ProgressBar

Les [actions personnalisées](custom-actions.md) peuvent ajouter des informations de temps et de progression à un contrôle [ProgressBar](progressbar-control.md) . Pour plus d’informations sur la création d’une boîte de dialogue d’affichage des actions avec un ProgressBar, consultez [création d’un contrôle ProgressBar](authoring-a-progressbar-control.md).

notez que deux actions personnalisées doivent être ajoutées au package Windows Installer pour signaler avec précision le temps et les informations de progression dans le ProgressBar. Une action personnalisée doit être une action personnalisée différée. Cette action personnalisée doit terminer votre installation personnalisée et envoyer les quantités d’incréments individuels au contrôle [ProgressBar](progressbar-control.md) quand le programme d’installation exécute le script d’installation. La deuxième action personnalisée doit être une action personnalisée d’exécution immédiate qui informe le ProgressBar du nombre de graduations à ajouter au nombre total lors de la phase d’acquisition et de génération de script de l’installation.

**Pour ajouter une action personnalisée au ProgressBar**

1.  Décidez comment l’action personnalisée décrira sa progression. Par exemple, une action personnalisée qui installe des clés de Registre peut afficher un message de progression et mettre à jour le [ProgressBar](progressbar-control.md) chaque fois que le programme d’installation écrit une clé de registre.
2.  Chaque mise à jour effectuée par l’action personnalisée modifie la longueur du [ProgressBar](progressbar-control.md) à l’aide d’un incrément de constante. Spécifiez ou calculez le nombre de graduations dans chaque incrément. En général, une modification de la longueur du ProgressBar d’un battement correspond à l’installation d’un octet. Par exemple, si le programme d’installation installe environ 10000 octets lorsqu’il écrit une clé de Registre, vous pouvez spécifier qu’il y a 10000 graduations dans un intervalle.
3.  Spécifiez ou calculez le nombre total de graduations que l’action personnalisée ajoute à la longueur du [ProgressBar](progressbar-control.md). Le nombre de graduations ajoutées par l’action personnalisée est généralement calculé comme suit : (incrément de graduation) x (nombre d’éléments). Par exemple, si l’action personnalisée écrit 10 clés de Registre, le programme d’installation installe environ 100000 octets et le programme d’installation doit donc augmenter l’estimation de la longueur totale finale du ProgressBar de 100000 cycles.
    > [!Note]  
    > Pour calculer cette valeur dynamiquement, l’action personnalisée doit contenir une section qui est immédiatement exécutée pendant la génération du script. La quantité de cycles signalée par votre action personnalisée d’exécution différée doit être égale au nombre de graduations ajoutées au nombre total de cycles par l’action d’exécution immédiate. Si ce n’est pas le cas, le temps restant indiqué par le contrôle de texte TimeRemaining sera inexact.

     

4.  Séparez votre action personnalisée en deux sections de code : une section qui s’exécute pendant la phase de génération de script et une section qui s’exécute pendant la phase d’exécution de l’installation. Pour ce faire, vous pouvez utiliser deux fichiers ou un fichier par conditionnement sur le mode d’exécution du programme d’installation. L’exemple suivant utilise un fichier et vérifie l’état de l’installation. Les sections de l’exemple sont conditionnées pour s’exécuter selon que le programme d’installation est dans la phase d’exécution ou de génération de script de l’installation.
5.  La section qui s’exécute pendant la génération du script doit augmenter l’estimation de la longueur totale finale du [ProgressBar](progressbar-control.md) par le nombre total de graduations de l’action personnalisée. Pour ce faire, envoyez un message de progression **ProgressAddition** .
6.  La section qui s’exécute pendant la phase d’exécution de l’installation doit configurer le texte et les modèles de message pour informer l’utilisateur de ce que fait l’action personnalisée et pour indiquer au programme d’installation de mettre à jour le contrôle [ProgressBar](progressbar-control.md) . Par exemple, informez le programme d’installation de déplacer le ProgressBar d’un incrément vers le bas et d’envoyer un message de progression explicite avec chaque mise à jour. Il y a généralement une boucle dans cette section si l’action personnalisée installe un. À chaque étape de cette boucle, le programme d’installation peut installer un élément de référence tel qu’une clé de Registre et mettre à jour le contrôle ProgressBar
7.  ajoutez une action personnalisée d’exécution immédiate à votre package Windows Installer. Cette action personnalisée indique à [ProgressBar](progressbar-control.md) le montant à avancer pendant les phases d’acquisition et de génération de script de l’installation. Pour l’exemple suivant, la source est la DLL créée en compilant l’exemple de code et la cible est le point d’entrée, caprogress.
8.  ajoutez une action personnalisée d’exécution différée à votre package Windows Installer. Cette action personnalisée termine les étapes de l’installation proprement dite et informe le [ProgressBar](progressbar-control.md) de l’avancement de la barre au moment où le programme d’installation exécute le script d’installation. Pour l’exemple suivant, la source est la DLL créée en compilant l’exemple de code et la cible est le point d’entrée, caprogress.
9.  Planifiez les actions personnalisées entre [InstallInitialize](installinitialize-action.md) et [InstallFinalize](installfinalize-action.md) dans la table [InstallExecuteSequence](installexecutesequence-table.md) . L’action personnalisée différée doit être planifiée immédiatement après l’action personnalisée d’exécution immédiate. Le programme d’installation n’exécutera pas l’action personnalisée différée tant que le script n’est pas exécuté.

L’exemple suivant montre comment une action personnalisée peut être ajoutée au [ProgressBar](progressbar-control.md). La source des deux actions personnalisées est la DLL créée en compilant l’exemple de code et la cible des deux actions personnalisées est le point d’entrée, caprogress. Cet exemple n’apporte aucune modification réelle au système, mais utilise le ProgressBar comme si vous installiez 10 éléments de référence dont la taille est d’environ 10 000 octets. Le programme d’installation met à jour le message et le ProgressBar chaque fois qu’il installe un élément de référence.


```C++
#include <windows.h>
#include <msiquery.h>
#pragma comment(lib, "msi.lib")

// Specify or calculate the number of ticks in an increment
// to the ProgressBar
const UINT iTickIncrement = 10000;
 
// Specify or calculate the total number of ticks the custom 
// action adds to the length of the ProgressBar
const UINT iNumberItems = 10;
const UINT iTotalTicks = iTickIncrement * iNumberItems;
 
UINT __stdcall CAProgress(MSIHANDLE hInstall)
{
    // Tell the installer to check the installation state and execute
    // the code needed during the rollback, acquisition, or
    // execution phases of the installation.
  
    if (MsiGetMode(hInstall,MSIRUNMODE_SCHEDULED) == TRUE)
    {
        PMSIHANDLE hActionRec = MsiCreateRecord(3);
        PMSIHANDLE hProgressRec = MsiCreateRecord(3);

        // Installer is executing the installation script. Set up a
        // record specifying appropriate templates and text for
        // messages that will inform the user about what the custom
        // action is doing. Tell the installer to use this template and 
        // text in progress messages.
 
        MsiRecordSetString(hActionRec, 1, TEXT("MyCustomAction"));
        MsiRecordSetString(hActionRec, 2, TEXT("Incrementing the Progress Bar..."));
        MsiRecordSetString(hActionRec, 3, TEXT("Incrementing tick [1] of [2]"));
        UINT iResult = MsiProcessMessage(hInstall, INSTALLMESSAGE_ACTIONSTART, hActionRec);
        if ((iResult == IDCANCEL))
            return ERROR_INSTALL_USEREXIT;
              
        // Tell the installer to use explicit progress messages.
        MsiRecordSetInteger(hProgressRec, 1, 1);
        MsiRecordSetInteger(hProgressRec, 2, 1);
        MsiRecordSetInteger(hProgressRec, 3, 0);
        iResult = MsiProcessMessage(hInstall, INSTALLMESSAGE_PROGRESS, hProgressRec);
        if ((iResult == IDCANCEL))
            return ERROR_INSTALL_USEREXIT;
              
        //Specify that an update of the progress bar's position in
        //this case means to move it forward by one increment.
        MsiRecordSetInteger(hProgressRec, 1, 2);
        MsiRecordSetInteger(hProgressRec, 2, iTickIncrement);
        MsiRecordSetInteger(hProgressRec, 3, 0);
 
        // The following loop sets up the record needed by the action
        // messages and tells the installer to send a message to update
        // the progress bar.

        MsiRecordSetInteger(hActionRec, 2, iTotalTicks);
       
        for( int i = 0; i < iTotalTicks; i+=iTickIncrement)
        {
            MsiRecordSetInteger(hActionRec, 1, i);

            iResult = MsiProcessMessage(hInstall, INSTALLMESSAGE_ACTIONDATA, hActionRec);
            if ((iResult == IDCANCEL))
                return ERROR_INSTALL_USEREXIT;
          
            iResult = MsiProcessMessage(hInstall, INSTALLMESSAGE_PROGRESS, hProgressRec);
            if ((iResult == IDCANCEL))
                return ERROR_INSTALL_USEREXIT;
   
            //A real custom action would have code here that does a part
            //of the installation. For this sample, code that installs
            //10 registry keys.
            Sleep(1000);
                    
        }
        return ERROR_SUCCESS;
    }
    else
    {
        // Installer is generating the installation script of the
        // custom action.
  
        // Tell the installer to increase the value of the final total
        // length of the progress bar by the total number of ticks in
        // the custom action.
        PMSIHANDLE hProgressRec = MsiCreateRecord(2);

         MsiRecordSetInteger(hProgressRec, 1, 3);
            MsiRecordSetInteger(hProgressRec, 2, iTotalTicks);
        UINT iResult = MsiProcessMessage(hInstall, INSTALLMESSAGE_PROGRESS, hProgressRec);
           if ((iResult == IDCANCEL))
            return ERROR_INSTALL_USEREXIT;     
        return ERROR_SUCCESS;
     }
}
```



 

 



