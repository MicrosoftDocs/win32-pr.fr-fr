---
description: Vue d’ensemble de la gestion des erreurs lors de l’utilisation des interfaces de programmation d’applications (API) StylusInput.
ms.assetid: 7d7ff5b2-3eda-4570-96fe-b3b8f41ff69b
title: Considérations relatives à la gestion des erreurs pour l’API StylusInput
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35fa582a8dbf531588f6d3d0c142c4ec7b40a058
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127196315"
---
# <a name="error-handling-considerations-for-the-stylusinput-api"></a>Considérations relatives à la gestion des erreurs pour l’API StylusInput

Les exceptions non gérées levées par un plug-in sont interceptées par l’objet [**RealTimeStylus**](realtimestylus-class.md) . Lorsqu’un plug-in lève une exception, le workflow normal de données est interrompu. Objet **RealTimeStylus** :

1.  Crée un objet [ErrorData](/previous-versions/ms575221(v=vs.100)) (en code managé).
2.  Appelle la méthode d' [**erreur**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-error) (dans le code managé, soit la méthode [Microsoft. StylusInput. IStylusSyncPlugin. Error](/previous-versions/ms824754(v=msdn.10)) , soit [Microsoft. StylusInput. IStylusAsyncPlugin. Error](/previous-versions/ms824771(v=msdn.10)) ) du plug-in qui a levé l’exception.
3.  Appelle la méthode d' [**erreur**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-error) des plug-ins restants dans cette collection.
4.  Si le plug-in qui a levé l’exception est un plug-in synchrone, l’objet [ErrorData](/previous-versions/ms575221(v=vs.100)) (en code managé) est ajouté à la file d’attente de sortie.
5.  L’objet [**RealTimeStylus**](realtimestylus-class.md) reprend le traitement normal des données d’origine.

Si un plug-in lève une exception à partir de sa méthode d' [**erreur**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-error) , l’objet [**RealTimeStylus**](realtimestylus-class.md) intercepte l’exception, mais ne génère pas de nouvel objet [ErrorData](/previous-versions/ms575221(v=vs.100)) . Pour plus d’informations sur la façon dont la fonction ErrorData est ajoutée à la file d’attente, consultez [données de plug-in et classe RealTimeStylus](plug-in-data-and-the-realtimestylus-class.md).

L’objet [**RealTimeStylus**](realtimestylus-class.md) n’arrête pas le traitement des données à partir du flux de données du stylet lorsque l’un de ses plug-ins lève une exception. Selon votre conception, certains de vos plug-ins peuvent être amenés à s’abonner à la notification [ErrorData](/previous-versions/ms575221(v=vs.100)) et à modifier leur comportement lorsqu’une exception se produit.

 

 
