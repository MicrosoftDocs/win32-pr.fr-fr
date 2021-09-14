---
description: COM+ 1,5 introduit la possibilité d’utiliser des services COM+ sans composants.
ms.assetid: da93d164-234a-4d1e-b82c-f3f904bb8cb6
title: Concepts des services COM+ sans composants
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4d692657d33143b9437a9c8134260a8c32431cb
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127295075"
---
# <a name="com-services-without-components-concepts"></a>Concepts des services COM+ sans composants

COM+ 1,5 introduit la possibilité d’utiliser des services COM+ sans composants. Cela réduit considérablement les coûts de performances lors de l’utilisation de services COM+ à partir d’un environnement qui n’utilise pas de composants, et il élimine également la complexité liée à l’utilisation de ces services. Depuis IIS 6,0, IIS et ASP tirent parti de l’utilisation des services COM+ sans composants.

Les services COM+ ont été conçus à l’origine pour être utilisés avec les composants COM+. Toutefois, certains environnements de programmation ne sont pas basés sur des composants et nécessitent donc une surcharge importante pour l’utilisation des services COM+. Par exemple, avant la publication de COM+ 1,5, IIS devait créer des objets shim uniquement pour pouvoir utiliser les services de transactions COM+ dans les pages ASP. Les coûts de performances résultant de la création de ces objets incluent le stockage des données de configuration dans la métabase IIS et la base de données d’inscription COM+ (RegDB), ainsi que la communication supplémentaire entre la métabase IIS et le RegDB COM+ requis pour gérer efficacement les données de configuration.

Si IIS devait utiliser un deuxième service COM+, tel que la synchronisation, il devait créer un objet shim complètement différent pour ce faire. Pour utiliser à la fois les transactions COM+ et la synchronisation, un troisième type d’objet shim est nécessaire. La complexité de cette approche s’adapte à O (N2), ce qui rend l’implémentation de nouveaux services extrêmement difficile.

Avec l’introduction des services COM+ sans composants, les services nécessaires sont configurés via un objet instancié à partir de la classe. La classe [**CServiceConfig**](cserviceconfig.md) implémente les interfaces nécessaires pour configurer les différents services tout en offrant la flexibilité nécessaire pour prendre en charge plusieurs services en même temps et la possibilité de prendre en charge de nouveaux services à l’avenir.

Les services configurés peuvent ensuite être utilisés par le biais de deux mécanismes différents : ils peuvent être utilisés par le biais de la fonction [**CoCreateActivity**](/windows/desktop/api/ComSvcs/nf-comsvcs-cocreateactivity) , qui applique les services à l’ensemble du travail soumis via l’activité créée par la fonction, et ils peuvent également être utilisés en incorporant le travail qui utilise les services entre les appels aux fonctions [**CoEnterServiceDomain**](/windows/desktop/api/ComSvcs/nf-comsvcs-coenterservicedomain) et [**CoLeaveServiceDomain**](/windows/desktop/api/ComSvcs/nf-comsvcs-coleaveservicedomain) . Aucune de ces fonctions ne nécessite la création de nouveaux composants pour pouvoir utiliser les services COM+. seul l’objet [**CServiceConfig**](cserviceconfig.md) est nécessaire.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Tâches des services COM+ sans composants](com--services-without-components-tasks.md)
</dt> </dl>

 

 



