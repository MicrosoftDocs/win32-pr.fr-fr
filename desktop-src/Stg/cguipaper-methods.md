---
title: Méthodes CGuiPaper
description: Les méthodes de CGuiPaper sont résumées comme suit. Ces méthodes sont toutes implémentées dans GUIPAPER. Cotisations.
ms.assetid: 965a60d4-2737-4a2d-8790-bee70bceaeeb
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1303ca38ffe02da0dc747e1a8834d36419452209
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103671670"
---
# <a name="cguipaper-methods"></a>Méthodes CGuiPaper

Les méthodes de CGuiPaper sont résumées comme suit. Ces méthodes sont toutes implémentées dans GUIPAPER. Cotisations.



| Méthode                                                         | Description                                                                                                           |
|----------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| BOOL init (HINSTANCE hInst, HWND hWnd, TCHAR \* pszCmdLineFile); | Initialise GuiPaper. Demande au serveur de créer un objet de copapiers.                                                     |
| HRESULT DrawOn (void);                                          | Verrouille le papier pour le dessin exclusif par ce client.                                                                   |
| HRESULT DrawOff (void);                                         | Déverrouille le papier pour permettre à d’autres clients de dessiner.                                                                         |
| HRESULT ClearWin (void);                                        | Efface la fenêtre d’affichage, mais conserve les données d’encre.                                                                           |
| HRESULT PaintWin (void);                                        | Efface la fenêtre et repeint avec les données d’encre actuelles.                                                                     |
| Effacement HRESULT (void);                                           | Efface le contenu de dessin actuel et efface la fenêtre d’affichage.                                                             |
| HRESULT Resize (WORD wWidth, WORD wHeight);                     | Redimensionne la fenêtre d’affichage.                                                                                           |
| HRESULT InkWidth (SHORT nInkWidth);                             | Définit la largeur d’encre actuelle pour le dessin.                                                                                   |
| HRESULT InkColor (COLORREF crInkColor);                         | Définit la couleur d’encre actuelle pour le dessin.                                                                                   |
| HRESULT InkSaving (BOOL bInkSaving);                            | Active et désactive l’enregistrement des données manuscrites dans le codocument.                                                                          |
| HRESULT InkStart (SHORT nX, SHORT nY);                          | Démarre la séquence de dessin de l’encre.                                                                                          |
| HRESULT InkDraw (SHORT nX, SHORT nY);                           | Dessine les données de séquence d’encre.                                                                                              |
| HRESULT InkStop (SHORT nX, SHORT nY);                           | Arrête la séquence de dessin de l’encre.                                                                                           |
| HRESULT ConnectPaperSink (void);                                | Connecte l’objet client PaperSink à la source de l’en-papiers du serveur.                                                    |
| HRESULT DisconnectPaperSink (void);                             | Déconnectez l’objet client PaperSink de la source de l’en-papiers du serveur.                                                |
| Chargement HRESULT (void);                                            | Charge des données manuscrites à partir du fichier composé actuel.                                                                            |
| HRESULT Save (void);                                            | Enregistre les données d’encre existantes dans le fichier composé actuel.                                                                     |
| HRESULT AskSave (void);                                         | Vérifie si le dessin a changé. Dans ce cas, affiche la boîte de dialogue demandant à l’utilisateur s’il faut enregistrer les modifications et y répondre de manière appropriée. |
| HRESULT Open (void);                                            | Affiche la boîte de dialogue commune Win32. Ouvre un fichier de données de papier existant.                                               |
| HRESULT SaveAs (void);                                          | Affiche la boîte de dialogue commune Win32. Enregistre les données du papier en cours dans le fichier renommé.                                              |
| COLORREF PickColor (void);                                      | Affiche la boîte de dialogue ommuns Win32. Demande à l’utilisateur de choisir une nouvelle couleur du stylet.                                                      |



 

La méthode **init** crée l’objet de codocumentation basé sur le serveur et affecte le \_ membre m pIPaper de CGuiPaper.

Les méthodes **AskSave**, **Open**, **SaveAs** et **PickColor** fournissent un comportement GUI familier à l’aide des boîtes de dialogue courantes Win32. Par exemple, la méthode **Open** utilise la boîte de dialogue Win32 Open File Name pour demander à l’utilisateur de spécifier un nom de fichier à ouvrir.

Les méthodes de **chargement** et d' **enregistrement** seront traitées en détail plus loin dans cette visite guidée.

**InkSaving**, **InkStart**, **InkDraw** et **InkStop** sont les méthodes centrales pour la fonctionnalité de dessin de l’application **StoClien** . **StoClien** utilise ces méthodes CGuiPaper pour capturer, afficher et stocker les données de dessin interactives au fur et à mesure qu’elles se produisent sous le contrôle utilisateur. Elles effectuent un double rôle de peinture de l’image dessinée dans la fenêtre du client, ainsi que le passage des données de dessin au codocument sur le serveur. Convertit les données de dessin en paquets de données d’encre pour le stockage.

 

 




