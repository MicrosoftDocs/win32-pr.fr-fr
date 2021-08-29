---
description: Fonctions de notification
ms.assetid: 44f69e05-1f08-48da-abb7-7e0a96c0cd26
title: Fonctions de notification
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc6a0a45689bf7dbe4433b018e330278b9c275a567c47fbdd2aa1da82582df0a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119036487"
---
# <a name="notification-functions"></a>Fonctions de notification



| Fonction plate                                                                  | Méthode Wrapper                            | Remarques                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|--------------------------------------------------------------------------------|-------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| GpStatus WINGDIPAPI GdiplusNotificationHook (jeton ptr de sortie ULONG \_ \* )<br/> | Non appelé par les méthodes wrapper.<br/> | La fonction [**GdiplusStartup**](/windows/desktop/api/Gdiplusinit/nf-gdiplusinit-gdiplusstartup) retourne (dans son paramètre de sortie) un pointeur vers une structure [**GdiplusStartupOutput**](/windows/desktop/api/Gdiplusinit/ns-gdiplusinit-gdiplusstartupoutput) . L’un des membres de la structure est un pointeur vers une fonction de raccordement de notification qui a la même signature que GdiplusNotificationHook.<br/> Il existe deux façons d’appeler la fonction de raccordement de notification. vous pouvez utiliser le pointeur retourné par [**GdiplusStartup**](/windows/desktop/api/Gdiplusinit/nf-gdiplusinit-gdiplusstartup) ou appeler GdiplusNotificationHook. En fait, GdiplusNotificationHook vérifie simplement que vous avez supprimé le thread d’arrière-plan, puis appelle la fonction de raccordement de notification qui est retournée par **GdiplusStartup**.<br/> Le paramètre Token reçoit un identificateur que vous devez passer ultérieurement dans un appel correspondant à la fonction unhook de notification.<br/>                                                                                                                                         |
| VOID WINGDIPAPI GdiplusNotificationUnhook (ULONG \_ ptr Token)<br/>         | Non appelé par les méthodes wrapper.<br/> | La fonction [**GdiplusStartup**](/windows/desktop/api/Gdiplusinit/nf-gdiplusinit-gdiplusstartup) retourne (dans son paramètre de sortie) un pointeur vers une structure [**GdiplusStartupOutput**](/windows/desktop/api/Gdiplusinit/ns-gdiplusinit-gdiplusstartupoutput) . L’un des membres de la structure est un pointeur vers une fonction de décrochage de notification qui a la même signature que GdiplusNotificationUnhook.<br/> Il existe deux façons d’appeler la fonction de déraccordement de notification. vous pouvez utiliser le pointeur retourné par [**GdiplusStartup**](/windows/desktop/api/Gdiplusinit/nf-gdiplusinit-gdiplusstartup) ou appeler GdiplusNotificationUnhook. En fait, GdiplusNotificationUnhook vérifie simplement que vous avez supprimé le thread d’arrière-plan, puis appelle la fonction de déraccordement de notification qui est retournée par **GdiplusStartup**.<br/> Quand vous appelez la fonction de déraccordement de notification, transmettez le jeton que vous avez reçu précédemment d’un appel correspondant à la fonction de raccordement de notification. Si vous ne le faites pas, il y aura des fuites de ressources qui ne seront pas nettoyées avant la fin du processus.<br/> |



 

 

 




