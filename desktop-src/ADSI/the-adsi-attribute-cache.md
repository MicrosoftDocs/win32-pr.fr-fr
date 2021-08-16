---
title: Le cache des attributs ADSI
description: Le modèle d’objet ADSI fournit un cache d’attributs côté client pour chaque objet ADSI.
ms.assetid: 0d2b4117-11f2-4b39-8fe5-3b176e4256f4
ms.tgt_platform: multiple
keywords:
- ADSI du cache des attributs ADSI
- ADSI ADSI, utilisation, accès et manipulation des données avec ADSI, cache d’attributs
- attributs ADSI, mise en cache des attributs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d5940d431fc476fdecd8397875bf06a04ed82ea30ab4ed2e98b94ccef98f0e9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119930043"
---
# <a name="the-adsi-attribute-cache"></a>Le cache des attributs ADSI

Le modèle d’objet ADSI fournit un cache d’attributs côté client pour chaque objet ADSI. Le cache des attributs est comparable à une table en mémoire qui contient les noms et les valeurs de la plupart des attributs d’objet qui ont été téléchargés. Certains attributs, tels que les attributs opérationnels, ne sont pas mis en cache. ADSI utilise la mise en cache de propriété pour améliorer les performances de manipulation d’attributs et ajouter une fonctionnalité de transaction pour les opérations de lecture et d’écriture d’attributs. cette fonctionnalité est essentielle pour les clients écrits dans des langages qui n’ont pas de mécanisme de traitement par lot natif pour définir des attributs, tels que le système de développement Microsoft Visual Basic. Sans le cache de propriété ADSI, ces clients doivent accéder au serveur chaque fois qu’un attribut est lu ou écrit.

Lorsqu’un objet est créé ou lié pour la première fois à, le cache de propriétés de l’objet est vide. Lorsque la méthode [**IADs :: GetInfo**](/windows/desktop/api/Iads/nf-iads-iads-getinfo) est appelée, ADSI charge les attributs demandés pour l’objet à partir du service d’annuaire sous-jacent dans le cache local. Lorsqu’une valeur d’attribut spécifique est lue et que le cache est vide, ADSI effectue un appel implicite à la méthode **IADs :: GetInfo** . Lorsque le cache est rempli, toutes les opérations de lecture d’attribut fonctionnent uniquement sur le contenu du cache.

Lorsqu’une valeur d’attribut est écrite, la nouvelle valeur est stockée dans le cache local jusqu’à ce que la méthode [**IADs :: setinfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) soit appelée. Lorsque la méthode **IADs :: setinfo** est appelée, les attributs du cache sont validés dans le service d’annuaire sous-jacent. Après l’appel de la méthode **IADs :: setinfo** , les valeurs restent dans le cache jusqu’à ce qu’elles soient explicitement actualisées avec un autre appel à la méthode [**IADs :: GetInfo**](/windows/desktop/api/Iads/nf-iads-iads-getinfo) .

> [!IMPORTANT]
> La méthode [**IADs :: GetInfo**](/windows/desktop/api/Iads/nf-iads-iads-getinfo) doit être utilisée avec précaution, car cette méthode remplacera toujours les valeurs d’attribut dans le cache à partir du service d’annuaire sous-jacent, même si la valeur mise en cache a été modifiée. Autrement dit, elle remplacera les valeurs d’attribut qui ont été modifiées dans le cache, mais non validées dans le service d’annuaire sous-jacent avec un appel à la méthode [**IADs :: setinfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) .

 

L’illustration suivante montre les différentes méthodes utilisées pour fonctionner sur le cache.

![cache d’attributs ADSI](images/ds2propc.png)

 

 




