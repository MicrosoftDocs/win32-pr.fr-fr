---
title: Contrôle Up-Down
description: Cette section contient des informations sur les éléments de programmation utilisés avec les contrôles Up-Up.
ms.assetid: 48c6b4bd-65b4-4388-959e-efffa7658274
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8364eb44ee01e27439c82d1d77e674bfb9e3165
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127115402"
---
# <a name="up-down-control"></a>Contrôle Up-Down

Cette section contient des informations sur les éléments de programmation utilisés avec les contrôles Up-Up.

### <a name="overviews"></a>Vues d'ensemble



| Rubrique                                    | Contenu                                                                                                                                                                                                            |
|------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Contrôles Up-Up](up-down-controls.md) | Un contrôle up-up est une paire de boutons fléchés sur lesquels l’utilisateur peut cliquer pour incrémenter ou décrémenter une valeur, telle qu’une position de défilement ou un nombre affiché dans un contrôle auxiliaire (appelé fenêtre associée).<br/> |



 

### <a name="functions"></a>Fonctions



| Rubrique                                              | Contenu                                                                                                                                                |
|----------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CreateUpDownControl**](/windows/desktop/api/Commctrl/nf-commctrl-createupdowncontrol) | Crée un contrôle up-up. Remarque : cette fonction est obsolète. Il s’agit d’une fonction 16 bits qui ne peut pas gérer les valeurs 32 bits pour la plage et la position.<br/> |



 

### <a name="messages"></a>Messages



| Rubrique                                                 | Contenu                                                                                                                                                                                                                               |
|-------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_GETACCEL UDM**](udm-getaccel.md)                 | Récupère les informations d’accélération pour un contrôle up-up. <br/>                                                                                                                                                                 |
| [**\_GETBASE (UDM**](udm-getbase.md)                   | Récupère la base de la base actuelle (c’est-à-dire, base 10 ou 16) pour un contrôle up-up. <br/>                                                                                                                                   |
| [**\_GETBUDDY UDM**](udm-getbuddy.md)                 | Récupère le handle de la fenêtre associée actuelle. <br/>                                                                                                                                                                          |
| [**\_GETPOS UDM**](udm-getpos.md)                     | Récupère la position actuelle d’un contrôle up-up avec une précision de 16 bits. <br/>                                                                                                                                                |
| [**\_GETPOS32 UDM**](udm-getpos32.md)                 | Retourne la position 32 bits d’un contrôle up-up.<br/>                                                                                                                                                                          |
| [**\_GETRANGE UDM**](udm-getrange.md)                 | Récupère les positions minimale et maximale (plage) pour un contrôle up-up. <br/>                                                                                                                                                |
| [**\_GETRANGE32 UDM**](udm-getrange32.md)             | Récupère la plage 32 bits d’un contrôle up-up. <br/>                                                                                                                                                                          |
| [**\_GETUNICODEFORMAT UDM**](udm-getunicodeformat.md) | Récupère l’indicateur de format de caractère Unicode pour le contrôle. <br/>                                                                                                                                                               |
| [**\_SETACCEL UDM**](udm-setaccel.md)                 | Définit l’accélération pour un contrôle up-up. <br/>                                                                                                                                                                              |
| [**\_SETBASE UDM**](udm-setbase.md)                   | Définit la base de base pour un contrôle up-up. La valeur de base détermine si la fenêtre associée affiche des nombres en chiffres décimaux ou hexadécimaux. Les nombres hexadécimaux sont toujours non signés et les nombres décimaux sont signés. <br/> |
| [**\_SETBUDDY UDM**](udm-setbuddy.md)                 | Définit la fenêtre associée pour un contrôle up-up. <br/>                                                                                                                                                                              |
| [**\_SetPos UDM**](udm-setpos.md)                     | Définit la position actuelle d’un contrôle up-up avec une précision de 16 bits. <br/>                                                                                                                                                    |
| [**\_SETPOS32 UDM**](udm-setpos32.md)                 | Définit la position d’un contrôle up-up avec une précision de 32 bits.<br/>                                                                                                                                                              |
| [**e \_ trange UDM**](udm-setrange.md)                 | Définit les positions minimale et maximale (plage) pour un contrôle up-up.<br/>                                                                                                                                                      |
| [**\_SETRANGE32 UDM**](udm-setrange32.md)             | Définit la plage de bits 32 d’un contrôle up-up. <br/>                                                                                                                                                                               |
| [**\_SETUNICODEFORMAT UDM**](udm-setunicodeformat.md) | Définit l’indicateur de format de caractère Unicode pour le contrôle. Ce message vous permet de modifier le jeu de caractères utilisé par le contrôle au moment de l’exécution plutôt que de devoir recréer le contrôle. <br/>                                   |



 

### <a name="notifications"></a>Notifications



| Rubrique                                                            | Contenu                                                                                                                                                                                                                                                                                                                                                       |
|------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [NM \_ RELEASEDCAPTURE (Up-Up)](nm-releasedcapture-up-down-.md) | Avertit une fenêtre parente d’un contrôle up-up que le contrôle libère la capture de la souris. Cette notification est envoyée sous la forme d’un message [**WM \_ Notify**](wm-notify.md) . <br/>                                                                                                                                                                       |
| [UDN \_ DELTAPOS](udn-deltapos.md)                                | Envoyé par le système d’exploitation à la fenêtre parente d’un contrôle up-up lorsque la position du contrôle est sur le point d’être modifiée. Cela se produit lorsque l’utilisateur demande une modification de la valeur en appuyant sur la flèche haut ou bas du contrôle. Le message [UDN \_ DELTAPOS](udn-deltapos.md) est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) . <br/> |



 

### <a name="structures"></a>Structures



| Rubrique                        | Contenu                                                                                                                                          |
|------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| [**NMUPDOWN**](/windows/win32/api/commctrl/ns-commctrl-nmupdown) | Contient des informations spécifiques aux messages de notification de contrôle up-out. Elle est identique à et remplace la structure de **\_ déverrouillage nm** . <br/> |
| [**UDACCEL**](/windows/desktop/api/Commctrl/ns-commctrl-udaccel)   | Contient des informations d’accélération pour un contrôle up-up. <br/>                                                                             |



 

### <a name="constants"></a>Constantes



| Rubrique                                                | Contenu                                                                      |
|------------------------------------------------------|-------------------------------------------------------------------------------|
| [Styles de contrôle up-up](up-down-control-styles.md) | Cette section répertorie les styles utilisés lors de la création de contrôles Up-Up.<br/> |



 

 

 





