---
description: la plupart des fonctionnalités de débogage décrites dans cette rubrique sont implémentées dans la bibliothèque de classes de base DirectShow. pour plus d’informations, consultez DirectShow les Classes de Base.
ms.assetid: 40b4f2ab-e629-41a0-b979-d74ac5fe83a2
title: filtres de DirectShow de débogage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e54532b68df09b78b3b03aa95d7dda5c84cdf7d770cffd131e47228e6d88cba2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118953288"
---
# <a name="debugging-directshow-filters"></a>filtres de DirectShow de débogage

la plupart des fonctionnalités de débogage décrites dans cette rubrique sont implémentées dans la bibliothèque de classes de base DirectShow. pour plus d’informations, consultez [DirectShow les Classes de Base](directshow-base-classes.md).

## <a name="assertion-checking"></a>Vérification des assertions

Utilisez la vérification d’assertion en toute libéralisation. Les assertions peuvent vérifier les hypothèses que vous apportez dans votre code sur les conditions préalables et post-conditions. DirectShow fournit plusieurs macros d’assertion. Pour plus d’informations, consultez [macros Assert et Breakpoint](assert-and-breakpoint-macros.md).

## <a name="object-names"></a>Noms d'objets

Dans les versions Debug, il existe une liste globale d’objets qui dérivent de la classe [**CBaseObject**](cbaseobject.md) . À mesure que des objets sont créés, ils sont ajoutés à la liste. Lorsqu’elles sont détruites, elles sont supprimées de la liste. Pour afficher une liste de ces objets, appelez la fonction [**DbgDumpObjectRegister**](dbgdumpobjectregister.md) .

La méthode de constructeur pour la classe de base [**CBaseObject**](cbaseobject.md) , et la plupart des classes dérivées de celle-ci, comprend un paramètre pour le nom de l’objet. Donnez à vos objets des noms uniques pour les identifier. Utilisez la macro [**Name**](name.md) lorsque vous déclarez le nom, afin que le nom soit alloué uniquement dans les versions Debug. Dans les versions commerciales, le nom devient **null**.

## <a name="debug-logging"></a>Journalisation du débogage

La fonction [**DbgLog**](dbglog.md) affiche les messages de débogage au fur et à mesure de l’exécution de votre programme. Utilisez cette fonction pour suivre l’exécution de votre application ou filtre. Vous pouvez consigner les codes de retour, les valeurs des variables et toute autre information pertinente.

Chaque message de débogage a un type, tel que trace du journal \_ ou erreur de journal \_ , et un niveau de débogage, qui indique l’importance du message. Les messages avec des niveaux de débogage inférieurs sont plus importants que ceux avec des niveaux supérieurs.

Dans l’exemple suivant, un filtre hypothétique déconnecte un code confidentiel d’un tableau de codes confidentiels. Si la tentative de déconnexion a échoué, le filtre affiche un message de trace du journal \_ . Si la tentative échoue, elle affiche un message d’erreur de journal \_ :


```C++
hr = m_PinArray[iPin]->Disconnect();
if (FAILED(hr))
{
    DbgLog((
        LOG_ERROR, 
        1, 
        TEXT("Could not disconnect pin %d. HRESULT = %#x", 
        iPin, 
        hr
        ));
 
   // Error handling code (not shown).
}
DbgLog((LOG_TRACE, 3, TEXT("Disconnected pin %d"), iPin));
```



Lors du débogage, vous pouvez définir le niveau de débogage pour chaque type de message. En outre, chaque module (DLL ou exécutable) conserve ses propres niveaux de débogage. Si vous testez un filtre, augmentez les niveaux de débogage de la DLL qui contient le filtre.

Pour plus d’informations, consultez [fonctions de sortie de débogage](debug-output-functions.md).

## <a name="critical-sections"></a>Sections critiques

Pour faciliter le suivi des blocages, incluez des assertions qui déterminent si le code appelant possède une section critique donnée. Les fonctions [**CritCheckIn**](critcheckin.md) et [**CritCheckOut**](critcheckout.md) indiquent si le thread appelant possède une section critique. En général, vous appelez ces fonctions à partir d’une macro Assert.

Vous pouvez également utiliser la fonction [**DbgLockTrace**](dbglocktrace.md) pour tracer le moment où les sections critiques sont conservées ou libérées.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Débogage dans DirectShow](debugging-in-directshow.md)
</dt> </dl>

 

 



