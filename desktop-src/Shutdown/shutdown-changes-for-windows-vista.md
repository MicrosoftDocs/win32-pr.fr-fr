---
description: Le tableau suivant résume les différences entre l’arrêt sur Windows Vista et Windows XP.
ms.assetid: da7985d2-85c8-47e1-a172-c9e92f450e24
title: Modifications de l’arrêt de Windows Vista
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e04bb20099349ce378384cf01c39e53ca03a896
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104034565"
---
# <a name="shutdown-changes-for-windows-vista"></a>Modifications de l’arrêt de Windows Vista

Le tableau suivant résume les différences entre l’arrêt sur Windows Vista et Windows XP.



| Fonctionnalité                 | Windows XP                                                                                                                                                                                                                                                                                                                                                                                | Windows Vista                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|-------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Blocage de l’arrêt       | Les applications peuvent retarder la réponse à [**WM \_ QUERYENDSESSION**](wm-queryendsession.md) pendant 5 secondes, puis le système autorise l’utilisateur à mettre fin à l’application. Les applications qui retournent la **valeur true** en réponse à **WM \_ QUERYENDSESSION** peuvent différer la réponse à [**WM \_ ENDSESSION**](wm-endsession.md) pendant 5 secondes, puis le système autorise l’utilisateur à mettre fin à l’application. | Les applications peuvent retarder la réponse à [**WM \_ QUERYENDSESSION**](wm-queryendsession.md) pendant 5 secondes, puis le système autorise l’utilisateur à continuer ou à annuler l’arrêt. Les applications qui retournent la **valeur true** en réponse à **WM \_ QUERYENDSESSION** peuvent différer la réponse à [**WM \_ ENDSESSION**](wm-endsession.md) pendant 5 secondes, puis le système autorise l’utilisateur à continuer ou à annuler l’arrêt.                                                                                                      |
| Annulation de l’arrêt      | Si une application retourne la **valeur false** en réponse à [**WM \_ QUERYENDSESSION**](wm-queryendsession.md), Shutdown est annulé dans la plupart des cas. Toutefois, aucune interface utilisateur n’est affichée. l’utilisateur peut donc ne pas savoir que l’arrêt a été annulé.                                                                                                                                                      | Si une application retourne la **valeur false** en réponse à [**WM \_ QUERYENDSESSION**](wm-queryendsession.md), elle apparaît toujours dans l’interface utilisateur d’arrêt. Notez que le système n’autorise pas les applications console ou les applications sans fenêtre visible à annuler l’arrêt. Ces applications sont automatiquement arrêtées si elles ne répondent pas à **WM \_ QUERYENDSESSION** ou [**WM \_ ENDSESSION**](wm-endsession.md) dans les 5 secondes ou si elles retournent **false** en réponse à **WM \_ QUERYENDSESSION**. |
| Arrêter l’interface utilisateur | Le système affiche une boîte de dialogue pour chaque arrêt bloquant de l’application. Si l’utilisateur clique sur le bouton **Terminer maintenant** , l’application est arrêtée. Si l’utilisateur clique sur le bouton **Annuler** , Shutdown est annulé et l’application continue de s’exécuter.                                                                                                                                    | Le système affiche une interface utilisateur plein écran qui identifie toutes les applications bloquant l’arrêt et leurs raisons (si elles ont inscrit une raison à l’aide de [**ShutdownBlockReasonCreate**](/windows/desktop/api/Winuser/nf-winuser-shutdownblockreasoncreate)).                                                                                                                                                                                                                                                                    |



 

## <a name="best-practices"></a>Bonnes pratiques

-   Les applications ne doivent pas bloquer l’arrêt. Répondez à [**WM \_ QUERYENDSESSION**](wm-queryendsession.md) aussi rapidement que possible et reportez les activités de nettoyage jusqu’à ce que le message [**WM \_ ENDSESSION**](wm-endsession.md) soit traité.
-   Les applications qui doivent bloquer l’arrêt doivent utiliser la nouvelle fonction [**ShutdownBlockReasonCreate**](/windows/desktop/api/Winuser/nf-winuser-shutdownblockreasoncreate) pour inscrire une chaîne expliquant la raison de l’utilisateur. L’utilisateur peut décider s’il faut continuer ou annuler l’arrêt.
-   Les applications ne peuvent pas s’appuyer sur la possibilité de bloquer l’arrêt.

 

 



