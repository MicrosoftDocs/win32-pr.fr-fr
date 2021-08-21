---
title: Étendue de la requête
description: L’étendue d’une requête est déterminée par l’objet auquel vous vous liez.
ms.assetid: 7ece8599-8a4b-45a1-95f4-a4180052f245
ms.tgt_platform: multiple
keywords:
- étendue de l’ADSI de requête
- interroge ADSI, Scope
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45a31ebe378502dd9b4ddda6dce83e3547dab580360a8d1ec07516d1e3347cf0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119023250"
---
# <a name="scope-of-query"></a>Étendue de la requête

L’étendue d’une requête est déterminée par l’objet auquel vous vous liez. Si vous ne savez pas où se trouve l’objet au sein de l’entreprise, vous devez effectuer une recherche aussi étendue que possible. Toutefois, si vous savez que l’objet sera contenu dans un domaine spécifique, tel que le domaine auquel l’utilisateur est connecté ou au sein d’un groupe spécifique, tel que le groupe Managers, vous devez définir l’étendue de la recherche pour qu’elle reflète les circonstances. Pour des performances optimales, vous devez essayer de cibler l’étendue pour rechercher le plus petit nombre d’objets possible.

Lorsque vous n’êtes pas certain de l’emplacement d’un objet dans l’entreprise, vous pouvez établir une liaison avec le service de catalogue global. Le service de catalogue global contient une liste de tous les objets de l’annuaire et un petit sous-ensemble des attributs de chaque objet. Une fois que vous avez trouvé l’objet dans le catalogue global, vous pouvez récupérer son nom unique à partir du catalogue global et l’utiliser pour établir une liaison à l’objet afin d’effectuer d’autres opérations.

Une fois que vous avez choisi l’objet à lier, vous pouvez restreindre davantage la requête à l’une des étendues suivantes : une requête de base, une requête à un niveau ou une recherche de sous-arborescence, comme indiqué dans l’illustration suivante.

![objets à la racine d’une recherche pour une recherche de base, d’un niveau ou d’une sous-arborescence](images/netds6.png)

## <a name="base"></a>Base

Une requête de base limite la recherche à l’objet de base uniquement. Le nombre maximal d’objets retournés est toujours un. Cette recherche peut être utilisée pour vérifier l’existence d’un objet. Par exemple, si vous avez un nom unique d’objet et que vous devez vérifier l’existence de l’objet en fonction du chemin d’accès, vous pouvez utiliser une recherche à un niveau. Si la recherche échoue, vous pouvez supposer que l’objet a peut-être été renommé ou déplacé vers un autre emplacement ou que des données incorrectes concernant l’objet ont été fournies. N’oubliez pas que vous devez stocker le GUID à la place du nom unique si vous souhaitez revisiter un objet. Cela permet à l’objet d’être renommé ou déplacé dans la hiérarchie de répertoires sans rompre le lien persistant.

## <a name="one-level"></a>Dossier parent

Une recherche à un niveau est limitée aux enfants immédiats d’un objet de base, mais exclut l’objet de base lui-même. Ce paramètre peut effectuer une recherche ciblée d’objets enfants immédiats d’un objet parent. Par exemple, si vous avez un objet parent appelé P1, et que ses enfants immédiats sont : C1, C2, C3, puis dans une recherche à un niveau, C1, C2 et C3 doivent être inclus lors de l’évaluation des critères, mais P1 ne fait pas partie de la recherche. Une recherche à un niveau peut être utilisée pour énumérer tous les enfants d’un objet. En fait, dans certains fournisseurs ADSI, l’énumération [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer) se traduit par une recherche à un niveau.

## <a name="subtree"></a>Sous-arborescence

Une recherche de sous-arborescence, également appelée recherche détaillée, comprend tous les objets sous l’objet de base, à l’exclusion de l’objet de base lui-même. Cette recherche peut générer des références à d’autres serveurs. Cette recherche a la plus grande étendue et peut retourner un jeu de résultats volumineux. Si possible, recherchez au moins un attribut indexé et définissez les paramètres de référence (pour plus d’informations, consultez [performances et gestion des jeux de résultats volumineux](performance-and-handling-large-result-sets.md)) en fonction de vos critères de recherche. Il est également conseillé de faire en sorte que les résultats d’une recherche de sous-arborescence soient exécutés de façon asynchrone et paginé pour réduire la charge du serveur et l’efficacité du réseau. Une recherche de sous-arborescence est normalement utilisée pour rechercher des objets pour une étendue donnée. Par exemple, recherchez tous les utilisateurs dont les comptes expirent dans 30 jours ou moins.

 

 




