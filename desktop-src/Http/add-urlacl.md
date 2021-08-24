---
title: add urlacl
description: Réserve l’URL spécifiée pour les comptes et les utilisateurs non-administrateurs.
ms.assetid: 5d89dec3-26e6-4db8-b4cc-e9b933ac60c5
keywords:
- Ajouter urlacl HTTP
topic_type:
- apiref
api_name:
- add urlacl
api_type:
- NA
ms.topic: reference
ms.custom: snippet-project
ms.date: 07/29/2020
ms.openlocfilehash: e3f4c715df70255ede8bd9ca5fc23131102983f8a3aeeb25735d5fc81d5ad9b5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119638779"
---
# <a name="add-urlacl"></a>add urlacl

Réserve l’URL spécifiée pour les comptes et les utilisateurs non-administrateurs. La liste de contrôle d’accès discrétionnaire (DACL, Discretionary Access Control List) peut être spécifiée à l’aide d’un nom de compte avec les paramètres Listen et Delegate ou à l’aide d’une chaîne SDDL (Security Descriptor Definition Language).

``` syntax
add urlacl [url=]string
           [[user=]string
           {[[listen={yes|no}] [delegate={yes|no}]] | [sddl=]string}

 
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="_url__string"></span><span id="_URL__STRING"></span>
**[URL =] chaîne**
</dt> <dd>

Spécifie l’URL complète.

</dd> <dt>

<span id="_user__string"></span><span id="_USER__STRING"></span>
**[user =] chaîne**
</dt> <dd>

Spécifie le nom d’utilisateur ou de groupe d’utilisateurs.

</dd> <dt>

<span id="_listen__yes_no__"></span><span id="_LISTEN__YES_NO__"></span>**\[écouter = {oui \| non}\]**
</dt> <dd>

Spécifie l’une des valeurs suivantes :

-   Oui : permet à l’utilisateur d’inscrire des URL. Il s'agit de la valeur par défaut.
-   non : refuse à l’utilisateur d’inscrire des URL.

</dd> <dt>

<span id="_delegate__yes_no__"></span><span id="_DELEGATE__YES_NO__"></span>**\[délégué = {oui \| non}\]**
</dt> <dd>

Spécifie l’une des valeurs suivantes :

-   Oui : permet à l’utilisateur de déléguer des URL.
-   non : refuse à l’utilisateur de déléguer des URL. Il s'agit de la valeur par défaut.

</dd> <dt>

<span id="_sddl__string"></span><span id="_SDDL__STRING"></span>
**[SDDL =] chaîne**
</dt> <dd>

Spécifie la chaîne SDDL qui décrit la liste DACL.

</dd> </dl>

## <a name="examples"></a>Exemples

* add urlacl url=https://+:80/MyUri user=DOMAIN\\ user

* add urlacl url=https://www.contoso.com:80/MyUri user=DOMAIN\\user listen=yes

* add urlacl url=https://www.contoso.com:80/MyUri user=DOMAIN\\user delegate=no

 
## <a name="see-also"></a>Voir aussi

* [Commandes Netsh http](/windows-server/networking/technologies/netsh/netsh-http#add-urlacl)
 