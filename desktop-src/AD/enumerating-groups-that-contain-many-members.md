---
title: Énumération des groupes qui contiennent de nombreux membres
description: en savoir plus sur l’énumération des groupes de Azure Active Directory qui contiennent de nombreux membres à l’aide de la récupération incrémentielle des données (récupération de plage).
ms.assetid: 78f81b09-2223-4b74-b8d5-7a97494c0324
ms.tgt_platform: multiple
keywords:
- Énumération des groupes qui contiennent de nombreux membres Active Directory
- groupes Active Directory, énumération de groupes avec de nombreux membres
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 550ec2f4a77938b26e2273d468d3f9740d637249501aa2396fef3744cd105060
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118695137"
---
# <a name="enumerating-groups-that-contain-many-members"></a>Énumération des groupes qui contiennent de nombreux membres

Les membres d’un groupe sont stockés dans un attribut à valeurs multiples appelé **member**. L’attribut **member** peut contenir un grand nombre de valeurs. L’énumération des membres peut être inefficace lorsque le nombre de valeurs dans un attribut à valeurs multiples devient important. Le serveur limite également le nombre maximal de valeurs qui peuvent être extraites dans une seule requête. Cela signifie que si un groupe peut avoir plus de membres que ce qui peut être fourni par le serveur, la seule façon d’énumérer tous les membres est d’utiliser la récupération incrémentielle des données, appelée *récupération de plage*.

La récupération de plage implique de demander un nombre limité de valeurs d’attribut dans une seule requête. Le nombre de valeurs demandé doit être inférieur ou égal au nombre maximal de valeurs prises en charge par le serveur. Pour réduire le nombre de fois que la requête doit contacter le serveur, le nombre de valeurs demandé doit être aussi proche que possible de cette valeur maximale. Pour permettre à une application de fonctionner correctement avec tous les serveurs, vous devez utiliser un nombre maximal de 1000.

La version du serveur qui fournit les données demandées détermine le nombre maximal de valeurs qui peuvent être récupérées dans une seule requête. Le tableau suivant répertorie la version du serveur et le nombre maximal de valeurs qui peuvent être récupérées dans une seule requête.



| Version du système d’exploitation du serveur | Valeurs maximales récupérées |
|---------------------------------|--------------------------|
| Windows 2000                    | 1 000                     |
| Windows Server 2003             | 1500                     |



 

Pour plus d’informations sur la récupération de plages de valeurs d’attribut avec ADSI, consultez [récupération de plage d’attributs](/windows/desktop/ADSI/attribute-range-retrieval).

Pour plus d’informations sur la récupération de plages de valeurs d’attribut avec [System. DirectoryServices](/dotnet/api/system.directoryservices), consultez [énumération de membres dans un grand groupe](https://msdn.microsoft.com/library/ms180907(v=VS.80).aspx).

 

 