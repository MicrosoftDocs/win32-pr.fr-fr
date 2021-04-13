---
title: État persistant de l’objet
description: État persistant de l’objet
ms.assetid: 731fef03-d204-48e7-b33a-801e97a9d2c2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c08d4dd1175b5a7681f79fa9049772af245a031
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309530"
---
# <a name="persistent-object-state"></a>État persistant de l’objet

Certains objets COM peuvent enregistrer leur état interne lorsqu’un client le leur demande.

COM définit les normes par le biais desquelles les clients peuvent demander l’initialisation, le chargement et l’enregistrement d’objets dans un magasin de données (par exemple, un fichier plat, un stockage structuré ou la mémoire). Il incombe au client de gérer l’emplacement où les données persistantes de l’objet sont stockées, mais pas le format des données. Les objets COM qui adhèrent à ces normes sont appelés *objets persistants*.

Pour plus d'informations, voir les rubriques suivantes :

-   [Interfaces d’objets persistants](persistent-object-interfaces.md)
-   [Initialisation d’objets persistants](initializing-persistent-objects.md)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Clients et serveurs COM](com-clients-and-servers.md)
</dt> </dl>

 

 




