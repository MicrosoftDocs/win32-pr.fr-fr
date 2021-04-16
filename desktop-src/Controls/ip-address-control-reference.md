---
title: Contrôle d’adresse IP
description: Cette section contient des informations sur les éléments de programmation utilisés avec les contrôles d’adresse IP.
ms.assetid: vs|controls|~\controls\ipaddress\reflist.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c80fc87a12ce49038f4c1836e684fa0f8895bd0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104462122"
---
# <a name="ip-address-control"></a>Contrôle d’adresse IP

Cette section contient des informations sur les éléments de programmation utilisés avec les contrôles d’adresse IP.

### <a name="overviews"></a>Vues d'ensemble



| Rubrique                                          | Contenu                                                                                                                    |
|------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| [Contrôles d’adresse IP](ip-address-controls.md) | Un contrôle d’adresse IP (Internet Protocol) permet à l’utilisateur d’entrer une adresse IP dans un format facilement compréhensible.<br/> |



 

### <a name="macros"></a>Macros



| Rubrique                                         | Contenu                                                                                                                              |
|-----------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| [**PREMIÈRE \_ adresse IP**](/windows/desktop/api/Commctrl/nf-commctrl-first_ipaddress)   | Extrait la valeur du champ 0 à partir d’une adresse IP compressée Récupérée avec le message de l’aide de la fonction [**IPM \_**](ipm-getaddress.md) . <br/> |
| [**QUATRIÈME \_ adresse IP**](/windows/desktop/api/Commctrl/nf-commctrl-fourth_ipaddress) | Extrait la valeur du champ 3 à partir d’une adresse IP compressée Récupérée avec le message de l’aide de la fonction [**IPM \_**](ipm-getaddress.md) . <br/> |
| [**MAKEIPADDRESS**](/windows/desktop/api/Commctrl/nf-commctrl-makeipaddress)        | Compresse quatre valeurs d’octet en un seul LPARAM pouvant être utilisé avec le message [**IPM \_ SETADDRESS**](ipm-setaddress.md) . <br/>  |
| [**MAKEIPRANGE**](/windows/desktop/api/Commctrl/nf-commctrl-makeiprange)            | Compresse deux valeurs d’octet en un seul LPARAM pouvant être utilisé avec le message [**IPM \_ SetRange**](ipm-setrange.md) . <br/>       |
| [**DEUXIÈME \_ adresse IP**](/windows/desktop/api/Commctrl/nf-commctrl-second_ipaddress) | Extrait la valeur du champ 1 à partir d’une adresse IP compressée Récupérée avec le message de l’aide de la fonction [**IPM \_**](ipm-getaddress.md) . <br/> |
| [**TROISIÈME \_ adresse IP**](/windows/desktop/api/Commctrl/nf-commctrl-third_ipaddress)   | Extrait la valeur du champ 2 d’une adresse IP compressée extraite avec le message de l’aide de la fonction [**IPM \_**](ipm-getaddress.md) . <br/> |



 

### <a name="messages"></a>Messages



| Rubrique                                         | Contenu                                                                                                                              |
|-----------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| [**\_CLEARADDRESS IPM**](ipm-clearaddress.md) | Efface le contenu du contrôle d’adresse IP. <br/>                                                                            |
| [**maipm, \_ GETADDRESS**](ipm-getaddress.md)     | Obtient les valeurs d’adresse pour les quatre champs dans le contrôle d’adresse IP. <br/>                                                    |
| [**\_ISBLANK IPM**](ipm-isblank.md)           | Détermine si tous les champs du contrôle d’adresse IP sont vides. <br/>                                                             |
| [**\_SETADDRESS IPM**](ipm-setaddress.md)     | Définit les valeurs d’adresse pour les quatre champs dans le contrôle d’adresse IP. <br/>                                                    |
| [**IPM \_ SetFocus**](ipm-setfocus.md)         | Définit le focus clavier sur le champ spécifié dans le contrôle d’adresse IP. Tout le texte de ce champ est sélectionné. <br/> |
| [**IPM \_ SEtrange**](ipm-setrange.md)         | Définit la plage valide pour le champ spécifié dans le contrôle d’adresse IP. <br/>                                                   |



 

### <a name="notifications"></a>Notifications



| Rubrique                                     | Contenu                                                                                                                                                                                   |
|-------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [IPN \_ FIELDCHANGED](ipn-fieldchanged.md) | Envoyé lorsque l’utilisateur modifie un champ dans le contrôle ou passe d’un champ à un autre. Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) . <br/> |



 

### <a name="structures"></a>Structures



| Rubrique                              | Contenu                                                                                              |
|------------------------------------|-------------------------------------------------------------------------------------------------------|
| [**NMIPADDRESS**](/windows/win32/api/commctrl/ns-commctrl-nmipaddress) | Contient des informations pour le code de notification [IPN \_ FIELDCHANGED](ipn-fieldchanged.md) . <br/> |



 

 

 





