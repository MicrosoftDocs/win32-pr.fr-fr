---
description: Voici les fonctions COM+.
ms.assetid: fdeb70ff-17ae-4ee4-a8b1-7fffb65ba2b2
title: Fonctions COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b1f7ce33e729a12c37ff1f2dcef516ab13d9b69a
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2021
ms.locfileid: "106537191"
---
# <a name="com-functions"></a>Fonctions COM+

Voici les fonctions COM+.



| Fonction                                                                 | Description                                                                                                                             |
|--------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| [**CoCreateActivity**](/windows/desktop/api/ComSvcs/nf-comsvcs-cocreateactivity)                             | Crée une activité, pour exécuter un travail en traitement par lots de type synchrone ou asynchrone, pouvant utiliser des services COM+ sans créer obligatoirement un composant COM+. |
| [**CoEnterServiceDomain**](/windows/desktop/api/ComSvcs/nf-comsvcs-coenterservicedomain)                     | Permet d’entrer du code qui peut ensuite utiliser des services COM+.                                                                                     |
| [**CoGetDefaultContext**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetdefaultcontext)                       | Récupère une référence au contexte par défaut du cloisonnement spécifié.                                                                |
| [**CoLeaveServiceDomain**](/windows/desktop/api/ComSvcs/nf-comsvcs-coleaveservicedomain)                     | Utilisé pour conserver le code qui utilise les services COM+.                                                                                             |
| **ComPlusCompleteCbbSetup**               | Effectue une migration du catalogue sur l’ordinateur de destination.                                                                              |
| **GetComPlusPackageInstallStatus** | Indique si le Common Language Runtime (CLR) 64 bits est installé.                                                                |
| [**GetDispenserManager**](/windows/desktop/api/MtxDM/nf-mtxdm-getdispensermanager)                       | Récupère l’interface [**IDispenserManager**](/windows/desktop/api/ComSvcs/nn-comsvcs-idispensermanager) du gestionnaire du distributeur.                                             |
| [**GetManagedExtensions**](/windows/desktop/api/ComSvcs/nf-comsvcs-getmanagedextensions)                     | Détermine si la version installée de COM+ prend en charge les fonctionnalités spéciales fournies pour gérer les composants pris en charge (objets managés).    |
| [**GetObjectContext**](/windows/desktop/api/ComSvcs/nf-comsvcs-getobjectcontext)                             | Récupère une référence au contexte associé à l’objet COM+ actuel.                                                   |
| [**MTSCreateActivity**](/windows/desktop/api/ComSvcs/nf-comsvcs-mtscreateactivity)                           | Crée une activité dans un thread unique cloisonné pour effectuer un travail en traitement par lots synchrone ou asynchrone.                                        |
| [**RecycleSurrogate**](/windows/desktop/api/ComSvcs/nf-comsvcs-recyclesurrogate)                             | Recycle le processus appelant.                                                                                                           |
| [**SafeRef**](/windows/desktop/api/ComSvcs/nf-comsvcs-saferef)                                               | Périmé n’utilisez pas.                                                                                                                   |



 

 

 



