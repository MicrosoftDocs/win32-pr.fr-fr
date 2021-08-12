---
title: Séquences de touches
description: Une chaîne de séquence clé est un ensemble d’identificateurs de clé délimités par des virgules, qui sont utilisés pour simuler l’appui sur la touche et la séquence de mise en version d’un clavier standard de style « 101 ».
ms.assetid: 6f5301d1-af6e-4b43-8884-c76b2300ba92
keywords:
- Windows PC virtuels Virtual PC, séquences de touches
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b300c1d417bad30f7a0e06fd8cfb411184eb8f6b800549536c9b6452dcdfefa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118591444"
---
# <a name="key-sequences"></a>Séquences de touches

\[Windows Virtual PC ne peut plus être utilisé à partir de Windows 8. Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Une chaîne de séquence clé est un ensemble d’identificateurs de clé délimités par des virgules, qui sont utilisés pour simuler l’appui sur la touche et la séquence de mise en version d’un clavier standard de style « 101 ».

Si un identificateur de clé apparaît dans la chaîne sans modificateur précédent, un code appuyé sur une touche est simulé, suivi immédiatement par son code de sortie de clé correspondant. Les modificateurs de clé peuvent être utilisés pour modifier ce comportement.

Par exemple, le modificateur **UpDown** envoie le code appuyé sur la touche pour l’identificateur de clé suivant sans envoyer le code de sortie de clé. Cela est utile pour simuler les touches Ctrl, Alt et Maj lorsqu’elles sont maintenues pendant que d’autres touches sont envoyées. Pour libérer la clé, elle doit être incluse dans la chaîne de clé avec un modificateur **up** précédent.

## <a name="key-identifiers"></a>Identificateurs de clé

La liste suivante détaille les chaînes d’identificateur de clé valides. 

| Chaîne d’identificateur de clé | Signification                         |
|-----------------------|---------------------------------|
| Échappement de clé \_           | touche **Échap**                 |
| Touche \_ F1               | touche **F1**                  |
| Touche \_ F2               | touche **F2**                  |
| Touche \_ F3               | touche **F3**                  |
| Touche \_ F4               | touche **F4**                  |
| Touche \_ F5               | touche **F5**                  |
| Touche \_ F6               | touche **F6**                  |
| Touche \_ F7               | touche **F7**                  |
| Touche \_ F8               | touche **F8**                  |
| Touche \_ F9               | touche **F9**                  |
| Touche \_ F10              | touche **F10**                 |
| Touche \_ F11              | touche **F11**                 |
| Touche \_ F12              | touche **F12**                 |
| \_Sysreq clé           | clé **sysreq**              |
| Touche arrêt \_ défil       | touche  arrêtée          |
| Saut de clé \_            | touche **Pause**               |
| \_LeftApostrophe clé   | la **\`** clé                  |
| Clé \_ 1                | touche **1**                   |
| Clé \_ 2                | touche **2**                   |
| Clé \_ 3                | touche **3**                   |
| Clé \_ 4                | touche **4**                   |
| Clé \_ 5                | touche **5**                   |
| Clé \_ 6                | touche **6**                   |
| Clé \_ 7                | touche **7**                   |
| Clé \_ 8                | touche **8**                   |
| Clé \_ 9                | touche **9**                   |
| Clé \_ 0                | touche **0**                   |
| \_Trait d’Union clé           | la **-** clé                   |
| Clé \_ égale           | la **=** clé                   |
| \_Retour arrière        | touche **retour arrière**           |
| Insertion de clé \_           | touche **ins**                 |
| Page d’hébergement des clés \_             | touche **début**                |
| Touche \_ PG. préc           | touche **PG. préc**              |
| Touche \_ Verr. num          | touche **Verr. num**             |
| Division du pavé numérique \_        | **/** touche du pavé numérique     |
| Multiplication du pavé numérique \_      | **\*** touche du pavé numérique    |
| Clavier \_ moins         | **-** touche du pavé numérique     |
| \_Onglet clé              | touche **Tab**                 |
| Touche \_ Q                | touche **Q**                   |
| Clé \_ W                | touche **W**                   |
| Clé \_ E                | touche **E**                   |
| Clé \_ R                | touche **R**                   |
| Clé \_ T                | touche **T**                   |
| Clé \_ Y                | touche **Y**                   |
| Clé \_ U                | touche **U**                   |
| Clé \_ I                | touche **I**                   |
| Clé \_ O                | touche **O**                   |
| Clé \_ P                | touche **P**                   |
| \_LeftBracket clé      | la **\[** clé                  |
| \_RightBracket clé     | la **\]** clé                  |
| \_Barre oblique inverse clé        | la **\\** clé                  |
| Suppression de clé \_           | la touche **Suppr**              |
| Fin de clé \_              | touche **fin**                 |
| Touche \_ PG. suiv         | touche **PG. suiv** .            |
| Pavé numérique \_ 7             | touche **7** du pavé numérique     |
| Pavé numérique \_ 8             | touche **8** du pavé numérique     |
| Pavé numérique \_ 9             | touche **9** du pavé numérique     |
| Clavier \_ plus          | **+** touche du pavé numérique     |
| Clé \_ A                | touche **A**                   |
| Clé \_ S                | la touche **S**                   |
| Clé \_ D                | touche **D**                   |
| Clé \_ F                | touche **F**                   |
| Clé \_ G                | touche **G**                   |
| Clé \_ H                | touche **H**                   |
| Clé \_ J                | touche **J**                   |
| Clé \_ K                | touche **K**                   |
| Clé \_ L                | touche **l**                   |
| \_Point-virgule clé        | clé **;**                   |
| \_SingleQuote clé      | la **touche**                   |
| Touche \_ entrée            | touche **entrée**               |
| Pavé numérique \_ 4             | touche **4** du pavé numérique     |
| Pavé numérique \_ 5             | touche **5** du pavé numérique     |
| Pavé numérique \_ 6             | touche **6** du pavé numérique     |
| \_MAJ clé        | la touche **MAJ de gauche**          |
| Touche \_ Z                | la touche **Z**                   |
| Clé \_ X                | touche **X**                   |
| Clé \_ C                | touche **C**                   |
| Clé \_ V                | touche **V**                   |
| Clé \_ B                | touche **B**                   |
| Clé \_ N                | touche **N**                   |
| Clé \_ M                | touche **M**                   |
| \_Virgule clé            | la touche **,**                   |
| \_Période clé           | **.** key                   |
| \_Barre oblique clé            | la **/** clé                   |
| \_MAJ droite clé       | la touche **MAJ de droite**         |
| Touche \_ haut               | touche **haut**                  |
| Pavé numérique \_ 1             | touche **1** du pavé numérique     |
| Pavé numérique \_ 2             | touche **2** du pavé numérique     |
| Pavé numérique \_ 3             | touche **3** du pavé numérique     |
| Entrée du pavé numérique \_         | touche **entrée** du pavé numérique |
| \_LeftCtrl clé         | touche **CTRL de gauche**           |
| \_LeftWindows clé      | touche **Windows gauche**        |
| \_LeftAlt clé          | touche **ALT de gauche**            |
| \_Espace clé            | la touche **espace**               |
| \_RightAlt clé         | touche **ALT de droite**           |
| \_RightWindows clé     | touche de **Windows droite**       |
| \_RightCtrl clé        | touche **CTRL de droite**          |
| \_Application clé      | clé d' **application**         |
| Touche \_ gauche             | la touche **gauche**                |
| Touche \_ enfoncée             | touche **PG. suiv** .                |
| Clé \_ droite            | touche **droite**               |
| Pavé numérique \_ 0             | touche **0** du pavé numérique     |
| Pavé numérique \_ DecimalPoint  | **.** touche du pavé numérique     |



 

## <a name="key-modifiers"></a>Modificateurs de clé

La liste suivante répertorie les chaînes de modificateur de clé valides. 

| Chaîne de modificateur de clé | Signification                                                                                       |
|---------------------|-----------------------------------------------------------------------------------------------|
| INACTIF                | Envoie un code appuyé sur une touche pour l’identificateur de clé suivant sans envoyer de code de sortie de clé. |
| UP                  | Envoyer un code publié par clé pour l’identificateur de clé suivant.                                    |
| HOLD                | Interrompez 200 millisecondes avant de continuer à traiter le reste de la chaîne de séquence clé. |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**IVMKeyboard**](ivmkeyboard.md)
</dt> </dl>

 

 