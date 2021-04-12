---
title: Prise en main avec des messages tactiles Windows
description: Cette section explique les tâches associées à l’obtention de l’entrée tactile Windows pour fonctionner dans votre application.
ms.assetid: cd4e140e-a0b8-494f-82d9-bc0bfba55ecd
keywords:
- Tactile Windows, messages
- Tactile Windows, inscription pour une entrée tactile
- Windows Touch, test des numériseurs d’entrée
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b39048a4f9d643026396328093ae554c0eaa5d08
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104382094"
---
# <a name="getting-started-with-windows-touch-messages"></a>Prise en main avec des messages tactiles Windows

Cette section explique les tâches associées à l’obtention de l’entrée tactile Windows pour fonctionner dans votre application.

Les étapes suivantes sont généralement effectuées lors de l’utilisation de messages tactiles Windows :

1.  Testez les fonctionnalités du digitaliseur d’entrée.
2.  Inscrivez-vous pour recevoir des messages tactiles Windows.
3.  Gérer les messages.

Le message utilisé pour Windows Touch est [**WM \_ Touch**](wm-touchdown.md). Ce message indique les différents États de contact avec un digitaliseur.

## <a name="testing-the-capabilities-of-the-input-digitizer"></a>Test des fonctionnalités du digitaliseur d’entrée

La fonction [GetSystemMetrics](/windows/win32/api/winuser/nf-winuser-getsystemmetrics) peut être utilisée pour interroger les fonctionnalités du digitaliseur d’entrée en passant la valeur *nIndex* du **\_ digitaliseur SM**. [GetSystemMetrics](/windows/win32/api/winuser/nf-winuser-getsystemmetrics) retourne un champ de bits qui indique si l’appareil est prêt, si ce dernier prend en charge PEN ou Touch, si le périphérique d’entrée est intégré ou externe, et si l’appareil prend en charge plusieurs entrées (Windows Touch). Le tableau suivant présente les bits des différents champs.



| bit   | 8           | 7           | 6        | 5        | 4            | 3              | 2              | 1                |
|-------|-------------|-------------|----------|----------|--------------|----------------|----------------|------------------|
| Valeur | Pile prête | Entrée multiple | Réservé | Réservé | Stylet externe | Stylet intégré | Interaction tactile externe | Fonctions tactiles intégrées |



 

Pour tester le résultat de la commande pour une fonctionnalité particulière, vous pouvez utiliser l’opérateur de & au niveau du bit et le bit particulier que vous testez. Par exemple, pour tester la fonction tactile Windows, vous devez vérifier que le bit septième ordre est défini (0x40 en hex). L’exemple de code suivant montre comment ces valeurs peuvent être testées.


```C++
#include <windows.h>
```




```C++
// test for touch
int value = GetSystemMetrics(SM_DIGITIZER);
if (value & NID_READY){ /* stack ready */}
if (value  & NID_MULTI_INPUT){
    /* digitizer is multitouch */ 
    MessageBoxW(hWnd, L"Multitouch found", L"IsMulti!", MB_OK);
}
if (value & NID_INTEGRATED_TOUCH){ /* Integrated touch */}
```



Le tableau suivant répertorie les constantes définies dans Windows. h pour le test des fonctions tactiles du digitaliseur d’entrée.



| Nom                   | Valeur      | Description                                                                                                                                                                                   |
|------------------------|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| configuration de tablette \_ \_ aucune   | 0x00000000 | Le digitaliseur d’entrée n’a pas de fonctionnalités tactiles.                                                                                                                                         |
| fonction \_ tactile intégrée nid \_ | 0x00000001 | Un digitaliseur tactile intégré est utilisé pour l’entrée.                                                                                                                                              |
| \_ \_ interface tactile externe nid   | 0x00000002 | Un digitaliseur tactile externe est utilisé pour l’entrée.                                                                                                                                                |
| \_ \_ stylet intégré nid   | 0x00000004 | Un digitaliseur de stylet intégré est utilisé pour l’entrée.                                                                                                                                                |
| \_ \_ stylet externe nid     | 0x00000008 | Un digitaliseur de stylet externe est utilisé pour l’entrée.                                                                                                                                                  |
| NID \_ multi- \_ entrée      | 0x00000040 | Un digitaliseur d’entrée avec prise en charge de plusieurs entrées est utilisé pour l’entrée.                                                                                                                        |
| NID \_ prêt             | 0x00000080 | Le digitaliseur d’entrée est prêt pour l’entrée. Si cette valeur est non définie, cela peut signifier que le service tablette est arrêté, que le digitaliseur n’est pas pris en charge ou que les pilotes du digitaliseur n’ont pas été installés. |



 

La vérification des \_ \* valeurs nid est un moyen utile de vérifier les capacités de l’ordinateur d’un utilisateur à configurer votre application pour l’entrée tactile, Pen ou non-tablette. Par exemple, si vous disposez d’une interface utilisateur dynamique et que vous souhaitez configurer automatiquement une partie de celle-ci, vous pouvez vérifier la valeur \_ tactile intégrée nid \_ , nid \_ tactile et peut obtenir le nombre maximal de touches à la première fois qu’un utilisateur exécute votre application.

> [!Note]  
> Il existe certaines limitations inhérentes à SM \_ GETSYSTEMMETRICS. Par exemple, le plug-and-Play n’est pas pris en charge. Pour cette raison, soyez prudent lors de l’utilisation de cette fonction comme moyen de configuration permanente.

 

## <a name="registering-to-receive-windows-touch-input"></a>Inscription pour recevoir des entrées tactiles Windows

Avant de recevoir des entrées tactiles Windows, les applications doivent d’abord s’inscrire pour recevoir des entrées tactiles Windows. En inscrivant la fenêtre de l’application, l’application indique qu’elle est compatible avec le toucher. Une fois que l’application a inscrit sa fenêtre, les notifications du pilote Windows Touch sont transférées à l’application lorsque l’entrée est effectuée dans la fenêtre. Lorsque l’application s’arrête, elle annule l’inscription de sa fenêtre pour désactiver les notifications.

> [!Note]  
> [**WM \_ Les messages TACTILEs**](wm-touchdown.md) sont actuellement « gourmands ». Une fois le premier message tactile reçu dans une fenêtre, tous les messages tactiles sont envoyés à cette fenêtre jusqu’à ce qu’une autre fenêtre reçoive le focus.

 

> [!Note]  
> Par défaut, vous recevez des messages de [**\_ mouvement WM**](wm-gesture.md) au lieu de messages [**WM \_ Touch**](wm-touchdown.md) . Si vous appelez [**RegisterTouchWindow**](/windows/desktop/api/winuser/nf-winuser-registertouchwindow), vous ne recevrez plus de messages de **\_ mouvement WM** .

 

Le code suivant montre comment une application peut s’inscrire pour recevoir des messages tactiles Windows dans une application Win32.


```C++
RegisterTouchWindow(hWnd, 0);
```



## <a name="handling-windows-touch-messages"></a>Gestion des messages tactiles Windows

Vous pouvez gérer les messages tactiles Windows à partir d’applications dans les systèmes d’exploitation Windows de nombreuses façons. Si vous programmez une application GUI, vous ajoutez du code dans la `WndProc` fonction pour gérer les messages qui vous intéressent. Si vous programmez une application MFC (Microsoft Foundation Class) ou une application managée, vous ajoutez des gestionnaires pour les messages qui vous intéressent. L’exemple de code suivant montre comment les messages tactiles peuvent être gérés à partir de WndProc dans une application Windows.


```C++
  LRESULT OnTouch(HWND hWnd, WPARAM wParam, LPARAM lParam ){
    BOOL bHandled = FALSE;
    UINT cInputs = LOWORD(wParam);
    PTOUCHINPUT pInputs = new TOUCHINPUT[cInputs];
    if (pInputs){
        if (GetTouchInputInfo((HTOUCHINPUT)lParam, cInputs, pInputs, sizeof(TOUCHINPUT))){
            for (UINT i=0; i < cInputs; i++){
                TOUCHINPUT ti = pInputs[i];
                //do something with each touch input entry
            }            
            bHandled = TRUE;
        }else{
             /* handle the error here */
        }
        delete [] pInputs;
    }else{
        /* handle the error here, probably out of memory */
    }
    if (bHandled){
        // if you handled the message, close the touch input handle and return
        CloseTouchInputHandle((HTOUCHINPUT)lParam);
        return 0;
    }else{
        // if you didn't handle the message, let DefWindowProc handle it
        return DefWindowProc(hWnd, WM_TOUCH, wParam, lParam);
    }
  }


LRESULT CALLBACK WndProc(HWND hWnd, UINT message, WPARAM wParam, LPARAM lParam)
{
    int wmId, wmEvent;
    PAINTSTRUCT ps;
    HDC hdc;

    switch (message)
    {
      // pass touch messages to the touch handler 
      case WM_TOUCH:
        OnTouch(hWnd, wParam, lParam);
        break;
```





Le code suivant montre comment vous pouvez implémenter la table des messages et un gestionnaire de messages. Notez que les messages doivent être déclarés dans la table des messages, puis que le gestionnaire du message doit être implémenté. Par exemple, dans une application MFC, elle peut être déclarée dans le code de la boîte de dialogue. Notez également que la `OnInitDialog` fonction pour votre fenêtre de boîte de dialogue doit inclure un appel à [**RegisterTouchWindow**](/windows/desktop/api/winuser/nf-winuser-registertouchwindow) , par exemple `RegisterTouchWindow(m_hWnd, 0)` .


```C++
  // Class implementations within a dialog
  LRESULT TestDlg::OnTouch( WPARAM wParam, LPARAM lParam ){
    //Insert handler code here to do something with the message or uncomment the following line to test
    //MessageBox(L"touch!", L"touch!", MB_OK);
    return 0;
  }
  // The message map
  BEGIN_MESSAGE_MAP()
    ON_WM_CREATE()
    ... ... ...
    ON_MESSAGE(WM_TOUCH, OnTouch)
  END_MESSAGE_MAP()  
 
  BOOL TestDlg::OnInitDialog()
  {
    CDialog::OnInitDialog();    

    RegisterTouchWindow(m_hWnd, 0);
     ... ... ...
  }  
  
```



Le toucher de la fenêtre indique les touches à partir d’une fenêtre indépendante.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Entrée tactile Windows](guide-multi-touch-input.md)
</dt> </dl>

 

 