---
title: Syntaxe d’attribut ADSI
description: Chaque attribut dans l’annuaire a une syntaxe associée. Par exemple, entier, chaîne, numérique, etc. ADSI définit sa propre syntaxe qui correspond à la syntaxe de répertoire native. Cette section décrit les types de syntaxe d’attribut dans ADSI.
ms.assetid: 83d3d42f-e35e-4bd1-b26e-d141e9ec9c31
ms.tgt_platform: multiple
keywords:
- attributs ADSI, syntaxe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b23d58b48b27fa88077f388b47535afd1dbd0a4f
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "103730213"
---
# <a name="adsi-attribute-syntax"></a>Syntaxe d’attribut ADSI

Chaque attribut dans l’annuaire a une syntaxe associée. Par exemple, entier, chaîne, numérique, etc. ADSI définit sa propre syntaxe qui correspond à la syntaxe de répertoire native. Cette section décrit les types de syntaxe d’attribut dans ADSI.

## <a name="distinguished-name-string"></a>Chaîne de nom unique


```VB
Syntax Type: ADSTYPE_DN_STRING
```



Le nom unique est utile pour lier deux objets ensemble. Par exemple, il peut créer un lien qui fait de l’objet Alice un gestionnaire de l’objet Bob. Si l’objet Alice se déplace vers un autre emplacement, le lien du gestionnaire entre Alice et Bob est automatiquement mis à jour.

Le nom unique doit contenir un objet de nom unique valide. Si le nom unique ne correspond pas à un objet existant valide, la plupart des serveurs rejettent la demande et renvoient une erreur de violation de contrainte.

Exemples :


```VB
Set x = GetObject("LDAP://CN=Bob, OU=Sales,DC=Fabrikam, DC=com)
x.Put "manager", "CN=Alice, OU=Sales, DC=Fabrikam, DC=COM"
x.SetInfo
 
PADS_ATTR_INFO pInfo;
// .. IDirectoryObject::GetObjectAttribute
printf("%S\n", pInfo->pADsValues->DNString );
```



## <a name="case-exact-string-and-case-ignore-string"></a>Chaîne de casse exacte et casse ignorée


```VB
Syntax Types: ADSTYPE_CASE_IGNORE_STRING, ADSTYPE_CASE_EXACT_STRING.
```



La chaîne de casse exacte est une chaîne respectant la casse alors que la chaîne de cas ignore est une chaîne ne respectant pas la casse. Un pourcentage important d’attributs dans l’annuaire utilisent cette syntaxe.

> [!Note]  
> Le répertoire peut ou non être stocké en tant que chaîne Unicode. Toutefois, ADSI accepte et retourne des chaînes Unicode.

 

Exemple :


```VB
Dim propList As IADsPropertyList
Set propList = GetObject("LDAP://DC=Fabrikam,DC=com")
Set propVal = New PropertyValue
 
' --- Property Value ---
propVal.CaseIgnoreString = "Fabrikam, Inc - Seattle, WA"
propVal.ADsType = ADSTYPE_CASE_IGNORE_STRING
```



## <a name="printable-string"></a>Chaîne imprimable


```VB
Syntax Type: ADSTYPE_PRINTABLE_STRING
```



Cette syntaxe est utilisée pour les attributs avec des valeurs de chaîne où les majuscules et les minuscules sont considérées comme inégales pour les comparaisons, par exemple, « FABRIKAM » et « Fabrikam » ne correspondent pas. ADSI accepte tout contenu pour une chaîne imprimable ; elle n’essaie pas de vérifier qu’elles sont effectivement imprimables.

## <a name="numeric-string"></a>Chaîne numérique


```VB
Syntax Type: ADSTYPE_NUMERIC_STRING
```



Dans cette syntaxe, les chaînes correspondent comme dans une chaîne imprimable, sauf que tous les espaces sont ignorés dans les comparaisons. ADSI n’effectue pas de vérification de valeur pour s’assurer que seuls les chiffres et les espaces apparaissent dans les valeurs de cette syntaxe. Active Directory accepte tout contenu pour une chaîne numérique ; il ne vérifie pas que les caractères sont numériques.

## <a name="utc-time"></a>Heure UTC


```VB
Syntax Type: ADSTYPE_UTC_TIME
```



Cette syntaxe stocke la date et l’heure dans une chaîne unique. Le format de chaîne se compose de trois parties concaténées : (1) AAMMJJ ; (2) HHMM ou HHMMSS (les deux sont acceptables); et (3) « Z » pour indiquer que l’heure donnée est l’heure GMT (Greenwich Mean Time), ou « +/-HHMM » pour indiquer que l’heure donnée est l’heure locale avec la valeur différentielle donnée par rapport à l’heure GMT. La différence est basée sur la formule suivante : GMT = local + différentielle.

> [!Note]  
> Les deux premiers chiffres de l’année ne sont pas stockés dans cette chaîne.

 

Voici quelques exemples de valeurs valides : « 9101311455Z », « 910131145503Z », « 9101314455-0500 », « 910131145503 + 0130 ». Cette chaîne est stockée en tant que caractères ASCII codés sur un octet, et aucun numéro de page de codes n’est stocké avec celle-ci.

Bien que le classement soit pris en charge, il n’est effectué qu’en tant que tri de chaîne non sensible à la casse ASCII, et non en interprétant correctement la signification des chaînes.

Toute valeur de chaîne valide est acceptée. Aucune tentative n’est effectuée pour s’assurer que la chaîne contient une chaîne d’heure valide.

## <a name="generalized-time"></a>Temps généralisé


```VB
Syntax Type: ADSTYPE_UTC_TIME
```



Si un nouvel attribut pour stocker des valeurs d’heure est défini, la syntaxe GeneralizedTime doit être utilisée. La syntaxe GeneralizedTime utilise quatre caractères pour représenter l’année au lieu de deux comme avec UTCTime.

Le format de la syntaxe GeneralizedTime est « AAAAMMJJHHMMSS. 0Z ». « 20010928060000.0 Z » est un exemple de valeur acceptable. Le « Z » indique qu’il n’y a pas de différence de temps. Active Directory stocke la date/l’heure sur l’heure GMT (Greenwich Mean Time). Si aucune différence de temps n’est spécifiée, la valeur par défaut est GMT.

Si l’heure est spécifiée dans un fuseau horaire différent de GMT, la différence entre le fuseau horaire et l’heure GMT est ajoutée à la chaîne au lieu de « Z » sous la forme « AAAAMMJJHHMMSS. 0 \[ +/- \] hhmm ». « 20010928060000.0 + 0200 » est un exemple de valeur acceptable.

La différence est basée sur la formule suivante : GMT = local + différentielle.

## <a name="boolean"></a>Boolean


```VB
Syntax Type: ADSTYPE_BOOLEAN
```



Active Directory accepte uniquement une valeur signée 32 bits pour cette syntaxe. Elle gère zéro comme **false** et toutes les valeurs autres que zéro comme **true**.

## <a name="integer"></a>Integer


```VB
Syntax Type: ADSTYPE_INTEGER
```



Valeur numérique signée 32 bits.

## <a name="large-integer"></a>Entier long


```VB
Syntax Type: ADSTYPE_LARGE_INTEGER
```



Valeur numérique signée 64 bits. Les entiers volumineux sont réellement implémentés en tant qu’objets COM sur l’interface [**IADsLargeInteger**](/windows/desktop/api/Iads/nn-iads-iadslargeinteger) . Les méthodes **HighPart** et **LowPart** sont utilisées pour accéder aux moitiés 2 32 bits de la valeur entière de type long.

Exemple :


```VB
Dim x as IADsLargeInteger
Set o = GetObject("LDAP://DC=Fabrikam,DC=com")
Set x = o.Get("UsnCreated")
Debug.Print x.HighPart
Debug.Print x.LowPart
```



## <a name="octet-string"></a>Chaîne d’octets


```VB
Syntax Type: ADSTYPE_OCTET_STRING
```



Une chaîne d’octets est retournée en tant que tableau variant d’octets. Cela se compose d’un nombre de tailles (nombre d’octets) suivi d’une série d’octets. Un octet est un octet de 8 bits, de sorte qu’une série d’octets est une chaîne de données binaires.

## <a name="object-class"></a>Classe d’objet


```VB
Syntax Type: ADSTYPE_CASE_IGNORE_STRING
```



La classe Object est un identificateur d’objet unique pour une classe de schéma donnée. La classe de chaque instance d’objet est identifiée par l’attribut **objectClass** . Une fois créée, vous ne pouvez jamais modifier une classe d’objet. **objectClass** est un attribut à valeurs multiples. Elle répertorie la classe spécifique de l’objet, ainsi que les classes de toutes les classes structurelles ou abstraites à partir desquelles la classe spécifique a été dérivée. Cela comprend top, la classe à partir de laquelle toutes les autres classes sont dérivées en fin de compte. Active Directory ne répertorie pas les classes auxiliaires dans l’attribut **objectClass** .

## <a name="security-descriptor"></a>Descripteur de sécurité


```VB
Syntax Type: ADSTYPE_NT_SECURITY_DESCRIPTOR
```



Les droits d’accès définissent les capacités d’un principal de sécurité lorsqu’il tente d’effectuer une opération sur un objet Active Directory. Un descripteur de sécurité décrit les informations de contrôle d’accès associées à un objet.

Le descripteur de sécurité est stocké en tant que propriété d’un objet d’annuaire dans la propriété **ntSecurityDescriptor** . Lorsqu’un utilisateur authentifié tente d’accéder à un objet d’annuaire, le serveur d’annuaire détermine l’accès accordé ou refusé à l’utilisateur en fonction du descripteur de sécurité de l’objet.

L’énumération [**\_ \_ \_ enum du contrôle SD ADS**](/windows/win32/api/iads/ne-iads-ads_sd_control_enum) spécifie des indicateurs de contrôle pour un descripteur de sécurité.

L’exemple de code suivant montre comment obtenir un descripteur de sécurité.


```VB
' Obtain a security descriptor.
Dim x as IADs
Dim sd as IADsSecurityDescriptor
Dim acl as IADsAccessControlList
 
Set x = GetObject("LDAP://DC=Fabrikam, DC=com")
Set sd = x.Get("nTSecurityDescriptor")
 
Debug.Print sd.Control
Debug.Print sd.Group
Debug.Print sd.Owner
Debug.Print sd.Revision
 
Set acl = sd.DiscretionaryAcl
Set sacl = sd.SystemAcl
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Syntaxes pour les attributs Active Directory](/windows/desktop/AD/syntaxes-for-attributes-in-active-directory-domain-services)
</dt> <dt>

[Choix d’une syntaxe](/windows/desktop/AD/choosing-a-syntax)
</dt> <dt>

[Comment spécifier des valeurs de comparaison](/windows/desktop/AD/how-to-specify-comparison-values)
</dt> </dl>

 

 