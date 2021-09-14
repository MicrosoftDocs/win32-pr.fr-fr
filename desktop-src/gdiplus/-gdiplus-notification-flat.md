---
description: Fonctions de notification
ms.assetid: 44f69e05-1f08-48da-abb7-7e0a96c0cd26
title: Fonctions de notification
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 84e5ca0bbcd9f2f184abd312fe15d4923e5cf14b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127007721"
---
# <a name="notification-functions"></a>Fonctions de notification



| Fonction plate                                                                  | Méthode Wrapper                            | Remarques                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|--------------------------------------------------------------------------------|-------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| GpStatus WINGDIPAPI GdiplusNotificationHook (jeton ptr de sortie ULONG \_ \* )<br/> | Non appelé par les méthodes wrapper.<br/> | La fonction [**GdiplusStartup**](/windows/desktop/api/Gdiplusinit/nf-gdiplusinit-gdiplusstartup) retourne (dans son paramètre de sortie) un pointeur vers une structure [**GdiplusStartupOutput**](/windows/desktop/api/Gdiplusinit/ns-gdiplusinit-gdiplusstartupoutput) . L’un des membres de la structure est un pointeur vers une fonction de raccordement de notification qui a la même signature que GdiplusNotificationHook.<br/> Il existe deux façons d’appeler la fonction de raccordement de notification. vous pouvez utiliser le pointeur retourné par [**GdiplusStartup**](/windows/desktop/api/Gdiplusinit/nf-gdiplusinit-gdiplusstartup) ou appeler GdiplusNotificationHook. En fait, GdiplusNotificationHook vérifie simplement que vous avez supprimé le thread d’arrière-plan, puis appelle la fonction de raccordement de notification qui est retournée par **GdiplusStartup**.<br/> Le paramètre Token reçoit un identificateur que vous devez passer ultérieurement dans un appel correspondant à la fonction unhook de notification.<br/>                                                                                                                                         |
| VOID WINGDIPAPI GdiplusNotificationUnhook (ULONG \_ ptr Token)<br/>         | Non appelé par les méthodes wrapper.<br/> | La fonction [**GdiplusStartup**](/windows/desktop/api/Gdiplusinit/nf-gdiplusinit-gdiplusstartup) retourne (dans son paramètre de sortie) un pointeur vers une structure [**GdiplusStartupOutput**](/windows/desktop/api/Gdiplusinit/ns-gdiplusinit-gdiplusstartupoutput) . L’un des membres de la structure est un pointeur vers une fonction de décrochage de notification qui a la même signature que GdiplusNotificationUnhook.<br/> Il existe deux façons d’appeler la fonction de déraccordement de notification. vous pouvez utiliser le pointeur retourné par [**GdiplusStartup**](/windows/desktop/api/Gdiplusinit/nf-gdiplusinit-gdiplusstartup) ou appeler GdiplusNotificationUnhook. En fait, GdiplusNotificationUnhook vérifie simplement que vous avez supprimé le thread d’arrière-plan, puis appelle la fonction de déraccordement de notification qui est retournée par **GdiplusStartup**.<br/> Quand vous appelez la fonction de déraccordement de notification, transmettez le jeton que vous avez reçu précédemment d’un appel correspondant à la fonction de raccordement de notification. Si vous ne le faites pas, il y aura des fuites de ressources qui ne seront pas nettoyées avant la fin du processus.<br/> |



 

 

 




