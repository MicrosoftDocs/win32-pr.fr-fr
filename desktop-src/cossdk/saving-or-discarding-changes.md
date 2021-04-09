---
description: Enregistrement ou rejet des modifications
ms.assetid: eba4e794-0929-450c-a172-6de6c2f2f2c4
title: Enregistrement ou rejet des modifications
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4946574facd0d41d68f4de8cf2f2f48410eb6e99
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103860849"
---
# <a name="saving-or-discarding-changes"></a>Enregistrement ou rejet des modifications

Lorsque vous définissez des propriétés sur un élément, aucune modification n’est réellement enregistrée dans le catalogue COM+ tant que vous n’avez pas enregistré explicitement les modifications. Pour ce faire, utilisez la méthode [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) sur l’objet [**COMAdminCatalogCollection**](comadmincatalogcollection.md) pour la collection contenant l’élément.

Si vous souhaitez ignorer les modifications qui n’ont pas encore été validées, vous pouvez appeler la méthode [**Populate**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-populate) sur l’objet [**COMAdminCatalogCollection**](comadmincatalogcollection.md) . Cela lit toutes les données persistantes du catalogue COM+ pour tous les éléments de la collection, en supprimant efficacement les modifications en attente.

Lorsque vous utilisez [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges), les incohérences dans les paramètres de propriété que vous avez choisi entraînent une erreur et **SaveChanges** ne parvient pas à écrire l’objet qui a retourné l’erreur. Toutes les propriétés d’un élément donné sont écrites ou ne peuvent pas être écrites dans leur ensemble.

Toutefois, lorsque des erreurs d’écriture se produisent, elles peuvent ne pas être dues à des paramètres incompatibles. une autre défaillance s’est peut-être produite. Vous devez inspecter les détails de l’échec pour être certain. Pour plus d’informations, consultez [gestion des erreurs d’administration com+](handling-com--administration-errors.md) et des [interdépendances entre les propriétés](interdependencies-between-properties.md).

En règle générale, plus vous essayez d’enregistrer en une seule fois, en particulier les modifications apportées à plusieurs objets, plus il est probable que vous obteniez une erreur et plus il est difficile d’effectuer le suivi.

En outre, entre les appels à [**remplir**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-populate) et [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges), vous n’avez pas de verrou sur les éléments de la collection ; les conflits sont possibles. Pour plus d’informations, consultez [obtention et définition des propriétés](getting-and-setting-properties.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Obtention et définition des propriétés](getting-and-setting-properties.md)
</dt> <dt>

[Interdépendances entre les propriétés](interdependencies-between-properties.md)
</dt> <dt>

[Interrogation des propriétés disponibles](querying-for-available-properties.md)
</dt> </dl>

 

 



