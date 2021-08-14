---
title: Traitement des résultats de la recherche
description: Après le premier appel à IDirectorySearch GetFirstRow ou IDirectorySearch GetNextRow, S \_ OK, s \_ ADS \_ \_ ou un résultat d’erreur est retourné.
ms.assetid: 3a84f394-a256-4815-901c-eaaae3d54b75
ms.tgt_platform: multiple
keywords:
- Traitement de l’AD des résultats de la recherche
- Active Directory, recherche, traitement des résultats de la recherche
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0a3ba7d3dac59e5d887dc7897eb6722295842f08cb4167d5292aaace0d115c0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118185203"
---
# <a name="processing-the-search-results"></a>Traitement des résultats de la recherche

Après le premier appel à [**IDirectorySearch :: GetFirstRow**](/windows/desktop/api/iads/nf-iads-idirectorysearch-getfirstrow) ou [**IDirectorySearch :: GetNextRow**](/windows/desktop/api/iads/nf-iads-idirectorysearch-getnextrow), les annonces sont **\_ incorrectes** ou **\_ \_ bien \_**, ou un résultat d’erreur est retourné.

Si la valeur de retour est « S », plus il y a de **\_ \_ \_ lignes**, plus aucun objet correspondant au filtre n’a été trouvé. Si un résultat d’erreur est retourné, la requête a échoué. Dans les deux cas, vous n’êtes pas obligé de traiter les lignes dans le résultat, car rien n’a été retourné.

Si la condition **S \_ OK** est retournée, une ligne a été récupérée. Vous pouvez analyser les colonnes par nom à l’aide de [**IDirectorySearch :: GetColumn**](/windows/desktop/api/iads/nf-iads-idirectorysearch-getcolumn). Le nom est le **lDAPDisplayName** de l’attribut dans la colonne. L’ensemble de toutes les colonnes a été défini par le paramètre pAttributeNames de la méthode [**IDirectorySearch :: ExecuteSearch**](/windows/desktop/api/iads/nf-iads-idirectorysearch-executesearch) . Si la **valeur null** a été spécifiée, le jeu de toutes les colonnes est l’Union de toutes les propriétés trouvées pour tous les objets retournés. Pour lire l’ensemble des colonnes retournées pour un objet, utilisez [**IDirectorySearch :: GetNextColumnName**](/windows/desktop/api/iads/nf-iads-idirectorysearch-getnextcolumnname) pour effectuer une itération sur chaque colonne et utilisez le nom de colonne retourné pour appeler **IDirectorySearch :: GetColumn**.

La méthode [**IDirectorySearch :: GetColumn**](/windows/desktop/api/iads/nf-iads-idirectorysearch-getcolumn) retourne une structure de [**\_ \_ colonne de recherche ADS**](/windows/desktop/api/iads/ns-iads-ads_search_column) qui contient le nom d’attribut, le type de l’attribut, le nombre de valeurs et un pointeur vers un tableau de structures [**ADSVALUE**](/windows/desktop/api/iads/ns-iads-adsvalue) qui contiennent les valeurs. Vous pouvez parcourir les structures **ADSVALUE** pour lire les valeurs de la propriété retournée par la colonne. Vous devez lire le membre approprié de la structure **ADSVALUE** en fonction du [**ADSTYPE**](/windows/win32/api/iads/ne-iads-adstypeenum) spécifié par le membre **dwADsType** de la structure de **\_ \_ colonne de recherche ADS** (ou du membre **dwType** de la structure **ADSVALUE** ). Par exemple, si **dwADsType** était **ADSTYPE \_ Integer**, vous devez lire le membre **Integer** de chaque structure **ADSVALUE** .

Pour plus d’informations et pour obtenir un exemple de code, consultez [exemple de code pour rechercher des utilisateurs](example-code-for-searching-for-users.md).

 

 