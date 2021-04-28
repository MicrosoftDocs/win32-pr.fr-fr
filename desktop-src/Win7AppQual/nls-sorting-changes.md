---
description: Modifications de tri NLS
ms.assetid: 24617b5f-14f1-4f1b-a288-7d20a8166da0
title: Modifications de tri NLS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e57cfaf2a9891c2d952637429786729670fc103c
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108088057"
---
# <a name="nls-sorting-changes"></a>Modifications de tri NLS

## <a name="affected-platforms"></a>Plateformes affectées

 **Clients** -Windows XP, Windows Vista, Windows 7  
**Serveurs** -windows Server 2003, windows Server 2008, windows Server 2008 R2  










## <a name="feature-impact"></a>Impact sur les fonctionnalités

 **Gravité** -haute  
**Frequency** : faible (peu d’applications affectées, mais si elles sont affectées, toujours endommagées)  


## <a name="description"></a>Description

Les fonctions NLS (National Language Support) aident les applications à prendre en charge les différents besoins propres aux langues et aux paramètres régionaux des utilisateurs dans le monde entier. Les nouvelles versions de Windows incluent presque invariablement les modifications NLS. Cette modification affecte le classement et le tri, et donc les applications qui ont des index persistants.

Une table de classement comporte deux nombres identifiant sa version (révision) : la version définie et la version NLS. Les deux versions sont des valeurs DWORD, composées d’une version majeure et d’une version mineure. Le premier octet d’une valeur est réservé, les deux octets suivants représentent la version principale et le dernier octet représente la version mineure. En termes hexadécimaux, le modèle est 0xRRMMMMmm, où R est égal à réservé, M est égal à principal et m est égal à mineur. Par exemple, une version majeure de 3 avec une version mineure de 4 est représentée sous la forme 0x304.

Pour une version majeure, un ou plusieurs points de code changent afin que l’application doive réindexer toutes les données pour que les comparaisons soient valides. Pour une version mineure, rien ne se déplace, mais des points de code sont ajoutés. Pour ce type de version, l’application doit uniquement réindexer les chaînes avec des valeurs précédemment non triées. En résumé, voici ce que signifient les numéros de version par rapport aux modifications apportées aux données dans les tables d’exceptions spécifiques aux paramètres régionaux et aux tables par défaut :

**NLSVersion majeures** : modification des points de code dans les tables « exception » ou spécifiques aux paramètres régionaux  
**NLSVersion mineur** – ajout de nouveaux points de code dans les tables « exception » ou spécifiques aux paramètres régionaux  
**DefinedVersion majeures** : points de code modifiés dans la table par défaut  
**DefinedVersion mineur** – ajout de nouveaux points de code dans la table par défaut  


**Tri des numéros de version pour les versions publiées :**



| Système d'exploitation    | Libérer           | Version (0xRRMMMMmm)         |
|---------------------|-------------------|------------------------------|
| Windows XP          | RTM/SP1/SP2/SP3/... | N/A-aucune API GetNLSVersion () |
| Windows Server 2003 | RTM/SP1           | 0x00 0000 01                 |
| Windows Vista       | RTM/SP1           | 0x00 0405 00                 |
| Windows Server 2008 | RTM               | 0x00 0501 00/0x00 5001 00  |
| Windows 7           | RTM               | 0x00060100                   |



 

## <a name="manifestation"></a>Manifestation

Les applications (telles que les bases de données) avec des index persistants qui ne vérifient pas la version NLS et la réindexation lors de la modification de la version ne peuvent pas être triées correctement ou ne peuvent pas fournir les résultats demandés.

Dans le cas d’interfaces utilisateur, les listes (par exemple, alphabétique, numérique, alphanumérique, symboles, etc.) peuvent être triées de manière incorrecte.

## <a name="solution"></a>Solution

Votre application peut appeler **GetNLSVersionEx** (Windows Vista ou version ultérieure) ou **GetNLSVersion** (avant Windows Vista) pour récupérer la version définie et la version nls pour une table de classement.

-   GetNLSVersionEx:

*Récupère des informations sur la version actuelle d’une fonctionnalité NLS spécifiée pour les paramètres régionaux spécifiés par le nom*  
Cette fonction permet à une application telle que Active Directory de déterminer si une modification NLS affecte les paramètres régionaux utilisés pour une table d’index particulière. Si ce n’est pas le cas, il n’est pas nécessaire de réindexer la table. Pour plus d’informations, consultez Gestion des paramètres régionaux et des informations de langue.  
Cette fonction prend en charge les paramètres régionaux personnalisés. Si *lpLocaleName* spécifie des paramètres régionaux supplémentaires, les données récupérées sont les données appropriées pour l’ordre de classement associé à ces paramètres régionaux supplémentaires.  

**Remarque :** Les versions de Windows antérieures à Windows Vista ne prennent pas en charge **GetNLSVersionEx**.  


-   GetNLSVersion (à utiliser pour les applications qui s’exécutent sur des versions de Windows antérieures à Windows Vista) :

*Récupère des informations sur la version actuelle d’une fonctionnalité NLS spécifiée pour les paramètres régionaux spécifiés par l’identificateur*  
Cette fonction permet à une application telle que Active Directory de déterminer si une modification NLS affecte l’identificateur de paramètres régionaux utilisé pour une table d’index particulière. Si ce n’est pas le cas, il n’est pas nécessaire de réindexer la table. Pour plus d’informations, consultez Gestion des paramètres régionaux et des informations de langue.  
**Remarque :** Cette fonction récupère des informations uniquement sur les paramètres régionaux spécifiés par l’identificateur. La fonction **GetNLSVersionEx** prend en charge les paramètres régionaux, les fonctionnalités et les noms RFC 4646 supplémentaires. Toutefois, les versions de Windows antérieures à Windows Vista ne prennent pas en charge **GetNLSVersionEx**.  
Les applications destinées à être exécutées uniquement sur Windows Vista et versions ultérieures doivent utiliser **GetNLSVersionEx** en préférence à cette fonction. **GetNLSVersionEx** fournit une prise en charge appropriée pour les paramètres régionaux supplémentaires.  


## <a name="compatibility-test"></a>Test de compatibilité

**Procédure de vérification de la modification d’une version de classement (autrement dit, vous devez réindexer) :**

-   **Utilisez GetNLSVersionEx ()** pour récupérer une structure **NLSVERSIONINFOEX** lors de l’indexation d’origine de vos données.
-   Stockez les propriétés suivantes avec votre index pour identifier la version :  **NLSVERSIONINFOEX. dwNLSVersion** et **NLSVERSIONINFOEX. dwDefinedVersion** : ces deux propriétés spécifient la version de la table de tri que vous utilisez.  
    **NLSVERSIONINFOEX. dwEffectiveId** : spécifie les paramètres régionaux effectifs de votre tri. Les paramètres régionaux personnalisés pointent vers un tri de paramètres régionaux dans la zone.  
    
-   Lorsque vous utilisez l’index **, utilisez GetNlsVersionEx ()** pour découvrir la version de vos données.
-   Si l’une des trois propriétés a changé, les données de tri que vous utilisez peuvent retourner des résultats différents et n’importe quelle indexation peut ne pas aboutir à la recherche d’enregistrements.
-   Si vous savez que vos données ne contiennent pas de points de code Unicode non valides (autrement dit, si toutes vos chaînes retournaient la **valeur true** à partir d’un appel à **IsNLSDefinedString ()**), vous pouvez les considérer comme étant identiques si seul l’octet de poids faible de **dwNLSVersion** et **dwDefinedVersion** a changé (les versions secondaires décrites ci-dessus).

## <a name="links-to-other-resources"></a>Liens vers d’autres ressources

-   [Internationalisation pour les applications Windows](../intl/international-support.md)
-   [GetNLSVersionEx fonction)](/windows/win32/api/winnls/nf-winnls-getnlsversionex)
-   [GetNLSVersion fonction)](/windows/win32/api/winnls/nf-winnls-getnlsversion)
-   [Comment savoir si la version de classement a changé](/archive/blogs/shawnste/)

 

 
