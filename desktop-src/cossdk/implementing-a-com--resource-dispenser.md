---
description: Implémentation d’un distributeur de ressources COM+
ms.assetid: 083c5962-f55a-435a-964e-fdc868f9bd3d
title: Implémentation d’un distributeur de ressources COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a81e189f3bfc5025bc949ef6e5bc82bf9408c339
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111434"
---
# <a name="implementing-a-com-resource-dispenser"></a>Implémentation d’un distributeur de ressources COM+

Les étapes suivantes décrivent une procédure générale pour l’implémentation d’un distributeur de ressources COM+ :

1.  Choisissez un format de **RESTYPID** qui catégorise les différences entre les ressources.

2.  Utilisez respectivement le fichier d’en-tête et la bibliothèque mtxdm. h et mtxdm. lib.

3.  Générez une DLL qui implémente l’interface [**IDispenserDriver**](/windows/desktop/api/ComSvcs/nn-comsvcs-idispenserdriver) et l’API que vous souhaitez exposer aux applications.

4.  Dans le démarrage ([*DllMain*](/windows/desktop/Dlls/dllmain) ou premier appel à l’API du distributeur), appelez la fonction [**GetDispenserManager**](/windows/desktop/api/MtxDM/nf-mtxdm-getdispensermanager) . Cela retourne un pointeur vers l’interface [**IDispenserManager**](/windows/desktop/api/ComSvcs/nn-comsvcs-idispensermanager) du gestionnaire du distributeur.

5.  Appelez [**IDispenserManager :: RegisterDispenser**](/windows/desktop/api/ComSvcs/nf-comsvcs-idispensermanager-registerdispenser), en passant un pointeur vers votre implémentation de [**IDispenserDriver**](/windows/desktop/api/ComSvcs/nn-comsvcs-idispenserdriver). Le gestionnaire de distribution crée alors un conteneur (gestionnaire de regroupement) pour votre distributeur de ressources, puis retourne le pointeur à votre interface [**IHolder**](/windows/desktop/api/ComSvcs/nn-comsvcs-iholder) .

6.  Stockez ce pointeur pour pouvoir appeler [**IHolder :: AllocResource**](/windows/desktop/api/ComSvcs/nf-comsvcs-iholder-allocresource) et [**IHolder :: FreeResource**](/windows/desktop/api/ComSvcs/nf-comsvcs-iholder-freeresource).

7.  Vous pouvez maintenant (en réponse aux appels à votre API) effectuer des appels à [**AllocResource**](/windows/desktop/api/ComSvcs/nf-comsvcs-iholder-allocresource) et [**FreeResource**](/windows/desktop/api/ComSvcs/nf-comsvcs-iholder-freeresource). **AllocResource** répond initialement en rappelant à votre méthode [**CreateResource**](/windows/desktop/api/ComSvcs/nf-comsvcs-idispenserdriver-createresource) , mais les appels **AllocResource** ultérieurs sont desservis à partir du pool de ressources en augmentation.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Concepts du distributeur de ressources COM+](com--resource-dispenser-concepts.md)
</dt> <dt>

[Interfaces du distributeur de ressources COM+](com--resource-dispenser-interfaces.md)
</dt> </dl>

 

 
