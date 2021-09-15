---
description: Gestion des erreurs d’administration COM+
ms.assetid: 03f00c19-ff81-478b-b545-048f3dbe5eda
title: Gestion des erreurs d’administration COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e7e5838d7fee7616a23f5e361df1aef65421492
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127519321"
---
# <a name="handling-com-administration-errors"></a>Gestion des erreurs d’administration COM+

Les erreurs générées lors de l’utilisation des objets comadmin sont signalées de deux manières, comme suit :

-   Utilisation de codes d’erreur spécifiques à la bibliothèque comadmin.
-   Utilisation des informations d’erreur étendues disponibles dans une collection [**errorInfo**](errorinfo.md) spéciale.

## <a name="error-codes"></a>Codes d’erreur

Vous gérez les codes d’erreur d’administration comme vous le feriez pour n’importe quel message d’erreur COM. dans Microsoft Visual C++, ces codes sont retournés en tant que valeurs **HRESULT** . dans Microsoft Visual Basic, elles sont levées en tant qu’exceptions que vous pouvez intercepter. Pour les programmeurs C++, les codes d’erreur d’administration COM+ sont définis dans Winerror. h. pour les programmeurs Visual Basic, ils sont disponibles via l’IDE Visual Basic.

## <a name="errorinfo-collection"></a>ErrorInfo, collection

Lorsqu’une erreur se produit, signalée par un code d’échec, des informations plus détaillées peuvent être disponibles, en fonction de la nature de l’erreur. Les objets comadmin fournissent des informations étendues dans les cas où la cause précise de l’échec est difficile à déterminer sans rapport détaillé, par exemple avec plusieurs opérations de lecture et d’écriture.

Par exemple, lorsque vous utilisez des méthodes telles que [**Populate**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-populate) et [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) sur un objet [**COMAdminCatalogCollection**](comadmincatalogcollection.md) , vous pouvez lire ou écrire des données pour chaque élément de la collection. Des erreurs compliquées peuvent se produire, et elles peuvent être difficiles à diagnostiquer en fonction d’un code d’erreur numérique unique. Par conséquent, la bibliothèque comadmin génère des informations d’erreur étendues par le biais d’une collection spéciale.

Quand des informations d’erreur étendues sont disponibles, elles sont placées dans la collection [**errorInfo**](errorinfo.md) qui est associée à la collection d’origine qui a rencontré l’erreur. Pour récupérer le rapport d’erreurs, récupérez la collection **errorInfo** qui est associée à la collection d’origine et examinez les éléments qu’elle contient. Vous pouvez récupérer la collection **errorInfo** à l’aide de [**GetCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-getcollection) sur [**COMAdminCatalogCollection**](comadmincatalogcollection.md), en laissant le deuxième paramètre vide à l’emplacement où vous spécifiez normalement la propriété de clé d’un élément parent.

Quand vous recevez une erreur, vous devez immédiatement obtenir et remplir la collection [**errorInfo**](errorinfo.md) pour la collection qui a échoué, sans effectuer d’autres opérations sur cette collection. Dans le cas contraire, la collection **errorInfo** est réinitialisée et ne détaille pas cette erreur.

Les éléments de la collection [**errorInfo**](errorinfo.md) exposent les propriétés spéciales de signalement d’erreurs MajorRef et MinorRef, qui détaillent la cause particulière de l’erreur. Pour plus d’informations, consultez **errorInfo**.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Opérations d’administration COM+ dans les transactions](com--administration-operations-within-transactions.md)
</dt> <dt>

[Exemple d’introduction utilisant le catalogue d’administration COM+](introductory-example-using-the-com--administration-catalog.md)
</dt> <dt>

[Vue d’ensemble des objets comadmin](overview-of-the-comadmin-objects.md)
</dt> <dt>

[Récupération des regroupements sur le catalogue COM+](retrieving-collections-on-the-com--catalog.md)
</dt> <dt>

[Définition des propriétés et enregistrement des modifications dans le catalogue COM+](setting-properties-and-saving-changes-to-the-com--catalog.md)
</dt> </dl>

 

 



