---
title: Liaison au catalogue global
description: Le catalogue global est un espace de noms qui contient des données d’annuaire pour tous les domaines d’une forêt.
ms.assetid: c3c131c7-d9dd-4dbd-a909-abd0ffd9f375
ms.tgt_platform: multiple
keywords:
- Liaison à l’AD du catalogue global
- AD du catalogue global, liaison à
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4d094a0c07a40fa063b726d0ba1c5a15977873d
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122881645"
---
# <a name="binding-to-the-global-catalog"></a>Liaison au catalogue global

Le catalogue global est un espace de noms qui contient des données d’annuaire pour tous les domaines d’une forêt. Le catalogue global contient un réplica partiel de chaque répertoire de domaine. Elle contient une entrée pour chaque objet de la forêt d’entreprise, mais elle ne contient pas toutes les propriétés de chaque objet. Au lieu de cela, elle contient uniquement les propriétés spécifiées pour l’inclusion dans le catalogue global.

Le catalogue global est stocké sur des serveurs spécifiques au sein de l’entreprise. Seuls les contrôleurs de domaine peuvent servir de serveurs de catalogue global. Les administrateurs indiquent si un contrôleur de domaine donné contient un catalogue global à l’aide du gestionnaire de sites et de services Active Directory.

Pour effectuer une liaison au catalogue global avec ADSI, utilisez le moniker « GC : ».

Il existe deux façons de lier le catalogue global pour effectuer une recherche dans une forêt :

-   Établissez une liaison avec l’objet racine d’entreprise pour effectuer une recherche dans tous les domaines de la forêt.
-   Effectuer une liaison à un objet spécifique pour rechercher cet objet et ses enfants. Par exemple, si vous établissez une liaison à un domaine qui a deux domaines sous celui-ci dans une arborescence de domaine de la forêt, vous pouvez effectuer une recherche dans ces trois domaines. N’oubliez pas que le nom unique de l’objet à lier est exactement le même que le nom unique utilisé pour la liaison à l’espace de noms « LDAP : ». Rappelez-vous que « LDAP : » est un réplica complet d’un domaine unique et que « GC : » est un réplica partiel de tous les domaines de la forêt.

Comme avec le moniker « LDAP : », vous pouvez utiliser une liaison sans serveur ou établir une liaison avec un serveur de catalogue global spécifique. Si vous recherchez dans la forêt Active, utilisez une liaison sans serveur. Toutefois, si vous effectuez une recherche dans une autre forêt, spécifiez un nom de domaine ou un serveur de catalogue global à lier, comme illustré dans les exemples suivants.

Liez à l’aide du nom de domaine :

``` syntax
GC://fabrikam.com
```

Liez à l’aide du nom du serveur :

``` syntax
GC://servername
```

Vous pouvez également effectuer une liaison à un objet spécifique dans le catalogue global. Pour effectuer une liaison à l’objet Sales dans le domaine fabrikam, utilisez le format suivant.

``` syntax
GC://fabrikam.com/DC=sales,DC=fabrikam,DC=com
```

Ou, pour effectuer une liaison à l’objet Sales sur le serveur, utilisez le format suivant.

``` syntax
GC://servername.fabrikam.com/DC=sales,DC=fabrikam,DC=com
```

**Pour effectuer une recherche dans l’ensemble de la forêt**

1.  Liez à la racine de l’espace de noms de catalogue global.
2.  Énumérez le conteneur de catalogue global. Le conteneur de catalogue global contient un seul objet que vous pouvez utiliser pour effectuer une recherche dans l’ensemble de la forêt.
3.  Utilisez l’objet dans le conteneur pour effectuer la recherche. En C/C++, appelez [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) pour recevoir un pointeur [**IDirectorySearch**](/windows/desktop/api/iads/nn-iads-idirectorysearch) sur l’objet afin de pouvoir utiliser l’interface **IDirectorySearch** pour effectuer la recherche. dans Visual Basic, utilisez l’objet retourné par l’énumération dans votre requête ADO.

Pour énumérer les serveurs de catalogue global d’un site, effectuez une recherche de sous-arborescence LDAP de « CN = &lt; yoursite &gt; , CN = sites <DN of the configurationNamingContext> », à l’aide de la chaîne de filtrage suivante.

``` syntax
(&(objectCategory=nTDSDSA)(options:1.2.840.113556.1.4.803:=1))
```

Ce filtre utilise le **\_ bit de règle de correspondance LDAP \_ \_ \_ et** l’opérateur de règle de correspondance (1.2.840.113556.1.4.803) pour rechercher les objets **nTDSDSA** dont le bit de poids faible est défini dans le masque de bits de l’attribut **options** . Le bit de poids faible, qui correspond à la constante de la valeur de l’option **nTDSDSA \_ OPT \_ is \_ GC** constant définie dans ntdsapi. h, identifie l’objet **nTDSDSA** d’un serveur de catalogue global. Pour plus d’informations sur les règles de correspondance, consultez [syntaxe de filtre de recherche](/windows/desktop/ADSI/search-filter-syntax).

Le parent de l’objet **nTDSDSA** est l’objet serveur et la propriété **dNSHostName** de l’objet Server est le nom DNS du serveur de catalogue global.

Vous ne pouvez pas utiliser \# définir des constantes telles que **nTDSDSA \_ OPT \_ est \_** un **bit de règle de correspondance LDAP et LDAP \_ \_ \_ \_ et** directement dans une chaîne de filtre de recherche. Toutefois, vous pouvez utiliser ces constantes comme arguments d’une fonction telle que [**swprintf \_ s**](/windows/win32/api/winuser/nf-winuser-wsprintfa) pour insérer les valeurs de constante dans une chaîne de filtrage.

Le catalogue global ne représente pas l’intégralité de l’arborescence de la forêt. Par exemple, vous pouvez vous attendre à ce que l’exemple de code suivant énumère tous les domaines de la forêt et tous les objets enfants de chaque domaine. En réalité, ce qu’il fait, c’est d’énumérer tous les domaines de la forêt, mais aucun des objets de domaine énumérés ne contient d’enfants. Il s’agit d’une limitation du catalogue global.


```VB
Dim oGC As IADs
Dim oDomain As IADs
Dim oChild As IADs

Set oGC = GetObject("GC:")
For Each oDomain In oGC
    ' Print the name of the domain.
    Debug.Print oDomain.Name
    
    ' Enumerate the child objects of the domain.
    For Each oChild In oDomain
        Debug.Print oChild.Name
    Next
Next
```



Pour résoudre ce cas, il est nécessaire de lier à chaque objet de domaine, puis d’énumérer les objets enfants de chaque domaine. La technique appropriée est présentée dans l’exemple de code suivant.


```VB
Dim oGC As IADs
Dim oDomainEnum As IADs
Dim oDomainBind As IADs
Dim oChild As IADs

Set oGC = GetObject("GC:")
For Each oDomainEnum In oGC
    ' Print the name of the domain.
    Debug.Print oDomainEnum.Name
    
    ' Bind to the domain.
    Set oDomainBind = GetObject("LDAP://" + oDomainEnum.Name)
    
    ' Enumerate the child objects of the domain.
    For Each oChild In oDomainBind
        Debug.Print oChild.Name
    Next
Next
```



Pour plus d’informations et des exemples de code qui montrent comment effectuer une recherche dans une forêt entière, consultez l' [exemple de code pour la recherche d’une forêt](example-code-for-searching-a-forest.md).

 

 
