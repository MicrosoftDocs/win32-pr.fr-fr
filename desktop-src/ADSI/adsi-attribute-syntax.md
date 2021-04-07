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
# <a name="adsi-attribute-syntax"></a><span data-ttu-id="26fae-107">Syntaxe d’attribut ADSI</span><span class="sxs-lookup"><span data-stu-id="26fae-107">ADSI Attribute Syntax</span></span>

<span data-ttu-id="26fae-108">Chaque attribut dans l’annuaire a une syntaxe associée.</span><span class="sxs-lookup"><span data-stu-id="26fae-108">Each attribute in the directory has an associated syntax.</span></span> <span data-ttu-id="26fae-109">Par exemple, entier, chaîne, numérique, etc.</span><span class="sxs-lookup"><span data-stu-id="26fae-109">For example, integer, string, numeric, and so on.</span></span> <span data-ttu-id="26fae-110">ADSI définit sa propre syntaxe qui correspond à la syntaxe de répertoire native.</span><span class="sxs-lookup"><span data-stu-id="26fae-110">ADSI defines its own syntax that maps to the native directory syntax.</span></span> <span data-ttu-id="26fae-111">Cette section décrit les types de syntaxe d’attribut dans ADSI.</span><span class="sxs-lookup"><span data-stu-id="26fae-111">This section describes the types of attribute syntaxes in ADSI.</span></span>

## <a name="distinguished-name-string"></a><span data-ttu-id="26fae-112">Chaîne de nom unique</span><span class="sxs-lookup"><span data-stu-id="26fae-112">Distinguished Name String</span></span>


```VB
Syntax Type: ADSTYPE_DN_STRING
```



<span data-ttu-id="26fae-113">Le nom unique est utile pour lier deux objets ensemble.</span><span class="sxs-lookup"><span data-stu-id="26fae-113">The distinguished name is useful for linking two objects together.</span></span> <span data-ttu-id="26fae-114">Par exemple, il peut créer un lien qui fait de l’objet Alice un gestionnaire de l’objet Bob.</span><span class="sxs-lookup"><span data-stu-id="26fae-114">For example, it can create a link that makes the Alice object a manager of the Bob object.</span></span> <span data-ttu-id="26fae-115">Si l’objet Alice se déplace vers un autre emplacement, le lien du gestionnaire entre Alice et Bob est automatiquement mis à jour.</span><span class="sxs-lookup"><span data-stu-id="26fae-115">If the Alice object moves to different place, the manager link between Alice and Bob is updated automatically.</span></span>

<span data-ttu-id="26fae-116">Le nom unique doit contenir un objet de nom unique valide.</span><span class="sxs-lookup"><span data-stu-id="26fae-116">The distinguished name must contain a valid distinguished name object.</span></span> <span data-ttu-id="26fae-117">Si le nom unique ne correspond pas à un objet existant valide, la plupart des serveurs rejettent la demande et renvoient une erreur de violation de contrainte.</span><span class="sxs-lookup"><span data-stu-id="26fae-117">If the distinguished name does not correspond to a valid existing object, most servers reject the request and return a constraint violation error.</span></span>

<span data-ttu-id="26fae-118">Exemples :</span><span class="sxs-lookup"><span data-stu-id="26fae-118">Examples:</span></span>


```VB
Set x = GetObject("LDAP://CN=Bob, OU=Sales,DC=Fabrikam, DC=com)
x.Put "manager", "CN=Alice, OU=Sales, DC=Fabrikam, DC=COM"
x.SetInfo
 
PADS_ATTR_INFO pInfo;
// .. IDirectoryObject::GetObjectAttribute
printf("%S\n", pInfo->pADsValues->DNString );
```



## <a name="case-exact-string-and-case-ignore-string"></a><span data-ttu-id="26fae-119">Chaîne de casse exacte et casse ignorée</span><span class="sxs-lookup"><span data-stu-id="26fae-119">Case Exact String and Case Ignore String</span></span>


```VB
Syntax Types: ADSTYPE_CASE_IGNORE_STRING, ADSTYPE_CASE_EXACT_STRING.
```



<span data-ttu-id="26fae-120">La chaîne de casse exacte est une chaîne respectant la casse alors que la chaîne de cas ignore est une chaîne ne respectant pas la casse.</span><span class="sxs-lookup"><span data-stu-id="26fae-120">Case Exact String is a case-sensitive string while Case Ignore String is a case-insensitive string.</span></span> <span data-ttu-id="26fae-121">Un pourcentage important d’attributs dans l’annuaire utilisent cette syntaxe.</span><span class="sxs-lookup"><span data-stu-id="26fae-121">A large percentage of attributes in the directory use this syntax.</span></span>

> [!Note]  
> <span data-ttu-id="26fae-122">Le répertoire peut ou non être stocké en tant que chaîne Unicode.</span><span class="sxs-lookup"><span data-stu-id="26fae-122">The directory may or may not store this as a Unicode string.</span></span> <span data-ttu-id="26fae-123">Toutefois, ADSI accepte et retourne des chaînes Unicode.</span><span class="sxs-lookup"><span data-stu-id="26fae-123">However, ADSI accepts and returns Unicode strings.</span></span>

 

<span data-ttu-id="26fae-124">Exemple :</span><span class="sxs-lookup"><span data-stu-id="26fae-124">Example:</span></span>


```VB
Dim propList As IADsPropertyList
Set propList = GetObject("LDAP://DC=Fabrikam,DC=com")
Set propVal = New PropertyValue
 
' --- Property Value ---
propVal.CaseIgnoreString = "Fabrikam, Inc - Seattle, WA"
propVal.ADsType = ADSTYPE_CASE_IGNORE_STRING
```



## <a name="printable-string"></a><span data-ttu-id="26fae-125">Chaîne imprimable</span><span class="sxs-lookup"><span data-stu-id="26fae-125">Printable String</span></span>


```VB
Syntax Type: ADSTYPE_PRINTABLE_STRING
```



<span data-ttu-id="26fae-126">Cette syntaxe est utilisée pour les attributs avec des valeurs de chaîne où les majuscules et les minuscules sont considérées comme inégales pour les comparaisons, par exemple, « FABRIKAM » et « Fabrikam » ne correspondent pas.</span><span class="sxs-lookup"><span data-stu-id="26fae-126">This syntax is used for attributes with string values where uppercase and lowercase are considered unequal for comparisons, for example, "FABRIKAM" and "Fabrikam" do not match.</span></span> <span data-ttu-id="26fae-127">ADSI accepte tout contenu pour une chaîne imprimable ; elle n’essaie pas de vérifier qu’elles sont effectivement imprimables.</span><span class="sxs-lookup"><span data-stu-id="26fae-127">ADSI accepts any contents for a Printable-String; it does not attempt to verify that they are indeed printable.</span></span>

## <a name="numeric-string"></a><span data-ttu-id="26fae-128">Chaîne numérique</span><span class="sxs-lookup"><span data-stu-id="26fae-128">Numeric String</span></span>


```VB
Syntax Type: ADSTYPE_NUMERIC_STRING
```



<span data-ttu-id="26fae-129">Dans cette syntaxe, les chaînes correspondent comme dans une chaîne imprimable, sauf que tous les espaces sont ignorés dans les comparaisons.</span><span class="sxs-lookup"><span data-stu-id="26fae-129">In this syntax, strings match as in Printable String, except that all space characters are ignored in comparisons.</span></span> <span data-ttu-id="26fae-130">ADSI n’effectue pas de vérification de valeur pour s’assurer que seuls les chiffres et les espaces apparaissent dans les valeurs de cette syntaxe.</span><span class="sxs-lookup"><span data-stu-id="26fae-130">ADSI does not perform value checking to ensure that only numerals and spaces appear in values of this syntax.</span></span> <span data-ttu-id="26fae-131">Active Directory accepte tout contenu pour une chaîne numérique ; il ne vérifie pas que les caractères sont numériques.</span><span class="sxs-lookup"><span data-stu-id="26fae-131">Active Directory accepts any content for a numeric string; it does not verify that the characters are numeric.</span></span>

## <a name="utc-time"></a><span data-ttu-id="26fae-132">Heure UTC</span><span class="sxs-lookup"><span data-stu-id="26fae-132">UTC Time</span></span>


```VB
Syntax Type: ADSTYPE_UTC_TIME
```



<span data-ttu-id="26fae-133">Cette syntaxe stocke la date et l’heure dans une chaîne unique.</span><span class="sxs-lookup"><span data-stu-id="26fae-133">This syntax stores the date and time in a single string.</span></span> <span data-ttu-id="26fae-134">Le format de chaîne se compose de trois parties concaténées : (1) AAMMJJ ; (2) HHMM ou HHMMSS (les deux sont acceptables); et (3) « Z » pour indiquer que l’heure donnée est l’heure GMT (Greenwich Mean Time), ou « +/-HHMM » pour indiquer que l’heure donnée est l’heure locale avec la valeur différentielle donnée par rapport à l’heure GMT.</span><span class="sxs-lookup"><span data-stu-id="26fae-134">The string format consists of three concatenated parts: (1) YYMMDD; (2) HHMM or HHMMSS (both are acceptable); and (3) "Z" to indicate that the time given is Greenwich Mean Time (GMT), or "+/-HHMM" to indicate that the time given is local time with the given differential from GMT.</span></span> <span data-ttu-id="26fae-135">La différence est basée sur la formule suivante : GMT = local + différentielle.</span><span class="sxs-lookup"><span data-stu-id="26fae-135">The differential is based on the formula: GMT=Local+differential.</span></span>

> [!Note]  
> <span data-ttu-id="26fae-136">Les deux premiers chiffres de l’année ne sont pas stockés dans cette chaîne.</span><span class="sxs-lookup"><span data-stu-id="26fae-136">The first two digits of the year are not stored in this string.</span></span>

 

<span data-ttu-id="26fae-137">Voici quelques exemples de valeurs valides : « 9101311455Z », « 910131145503Z », « 9101314455-0500 », « 910131145503 + 0130 ».</span><span class="sxs-lookup"><span data-stu-id="26fae-137">Some examples of legal values are "9101311455Z", "910131145503Z", "9101314455-0500", "910131145503+0130".</span></span> <span data-ttu-id="26fae-138">Cette chaîne est stockée en tant que caractères ASCII codés sur un octet, et aucun numéro de page de codes n’est stocké avec celle-ci.</span><span class="sxs-lookup"><span data-stu-id="26fae-138">This string is stored as single-byte ASCII characters, and no code page number is stored with it.</span></span>

<span data-ttu-id="26fae-139">Bien que le classement soit pris en charge, il n’est effectué qu’en tant que tri de chaîne non sensible à la casse ASCII, et non en interprétant correctement la signification des chaînes.</span><span class="sxs-lookup"><span data-stu-id="26fae-139">Although ordering is supported, it is done only as an ASCII case-insensitive string sort, not by properly interpreting the meaning of the strings.</span></span>

<span data-ttu-id="26fae-140">Toute valeur de chaîne valide est acceptée.</span><span class="sxs-lookup"><span data-stu-id="26fae-140">Any valid string value is accepted.</span></span> <span data-ttu-id="26fae-141">Aucune tentative n’est effectuée pour s’assurer que la chaîne contient une chaîne d’heure valide.</span><span class="sxs-lookup"><span data-stu-id="26fae-141">No attempt is made to ensure that the string contains a valid time string.</span></span>

## <a name="generalized-time"></a><span data-ttu-id="26fae-142">Temps généralisé</span><span class="sxs-lookup"><span data-stu-id="26fae-142">Generalized Time</span></span>


```VB
Syntax Type: ADSTYPE_UTC_TIME
```



<span data-ttu-id="26fae-143">Si un nouvel attribut pour stocker des valeurs d’heure est défini, la syntaxe GeneralizedTime doit être utilisée.</span><span class="sxs-lookup"><span data-stu-id="26fae-143">If a new attribute to store time values is being defined, the GeneralizedTime syntax should be used.</span></span> <span data-ttu-id="26fae-144">La syntaxe GeneralizedTime utilise quatre caractères pour représenter l’année au lieu de deux comme avec UTCTime.</span><span class="sxs-lookup"><span data-stu-id="26fae-144">GeneralizedTime syntax uses four characters to represent the year instead of two as with UTCTime.</span></span>

<span data-ttu-id="26fae-145">Le format de la syntaxe GeneralizedTime est « AAAAMMJJHHMMSS. 0Z ».</span><span class="sxs-lookup"><span data-stu-id="26fae-145">The format for the GeneralizedTime syntax is "YYYYMMDDHHMMSS.0Z".</span></span> <span data-ttu-id="26fae-146">« 20010928060000.0 Z » est un exemple de valeur acceptable.</span><span class="sxs-lookup"><span data-stu-id="26fae-146">An example of an acceptable value is "20010928060000.0Z".</span></span> <span data-ttu-id="26fae-147">Le « Z » indique qu’il n’y a pas de différence de temps.</span><span class="sxs-lookup"><span data-stu-id="26fae-147">The "Z" indicates no time differential.</span></span> <span data-ttu-id="26fae-148">Active Directory stocke la date/l’heure sur l’heure GMT (Greenwich Mean Time).</span><span class="sxs-lookup"><span data-stu-id="26fae-148">Active Directory stores date/time as Greenwich Mean Time (GMT).</span></span> <span data-ttu-id="26fae-149">Si aucune différence de temps n’est spécifiée, la valeur par défaut est GMT.</span><span class="sxs-lookup"><span data-stu-id="26fae-149">If no time differential is specified, GMT is the default.</span></span>

<span data-ttu-id="26fae-150">Si l’heure est spécifiée dans un fuseau horaire différent de GMT, la différence entre le fuseau horaire et l’heure GMT est ajoutée à la chaîne au lieu de « Z » sous la forme « AAAAMMJJHHMMSS. 0 \[ +/- \] hhmm ».</span><span class="sxs-lookup"><span data-stu-id="26fae-150">If the time is specified in a time zone other than GMT, the differential between the time zone and GMT is appended to the string instead of "Z" in the form "YYYYMMDDHHMMSS.0\[+/-\]HHMM".</span></span> <span data-ttu-id="26fae-151">« 20010928060000.0 + 0200 » est un exemple de valeur acceptable.</span><span class="sxs-lookup"><span data-stu-id="26fae-151">An example of an acceptable value is "20010928060000.0+0200".</span></span>

<span data-ttu-id="26fae-152">La différence est basée sur la formule suivante : GMT = local + différentielle.</span><span class="sxs-lookup"><span data-stu-id="26fae-152">The differential is based on the formula: GMT=Local+differential.</span></span>

## <a name="boolean"></a><span data-ttu-id="26fae-153">Boolean</span><span class="sxs-lookup"><span data-stu-id="26fae-153">Boolean</span></span>


```VB
Syntax Type: ADSTYPE_BOOLEAN
```



<span data-ttu-id="26fae-154">Active Directory accepte uniquement une valeur signée 32 bits pour cette syntaxe.</span><span class="sxs-lookup"><span data-stu-id="26fae-154">Active Directory accepts only a signed 32-bit value for this syntax.</span></span> <span data-ttu-id="26fae-155">Elle gère zéro comme **false** et toutes les valeurs autres que zéro comme **true**.</span><span class="sxs-lookup"><span data-stu-id="26fae-155">It handles zero as **FALSE** and all nonzero values as **TRUE**.</span></span>

## <a name="integer"></a><span data-ttu-id="26fae-156">Integer</span><span class="sxs-lookup"><span data-stu-id="26fae-156">Integer</span></span>


```VB
Syntax Type: ADSTYPE_INTEGER
```



<span data-ttu-id="26fae-157">Valeur numérique signée 32 bits.</span><span class="sxs-lookup"><span data-stu-id="26fae-157">A 32-bit signed numeric value.</span></span>

## <a name="large-integer"></a><span data-ttu-id="26fae-158">Entier long</span><span class="sxs-lookup"><span data-stu-id="26fae-158">Large Integer</span></span>


```VB
Syntax Type: ADSTYPE_LARGE_INTEGER
```



<span data-ttu-id="26fae-159">Valeur numérique signée 64 bits.</span><span class="sxs-lookup"><span data-stu-id="26fae-159">A 64-bit signed numeric value.</span></span> <span data-ttu-id="26fae-160">Les entiers volumineux sont réellement implémentés en tant qu’objets COM sur l’interface [**IADsLargeInteger**](/windows/desktop/api/Iads/nn-iads-iadslargeinteger) .</span><span class="sxs-lookup"><span data-stu-id="26fae-160">Large integers are actually implemented as COM objects on the [**IADsLargeInteger**](/windows/desktop/api/Iads/nn-iads-iadslargeinteger) interface.</span></span> <span data-ttu-id="26fae-161">Les méthodes **HighPart** et **LowPart** sont utilisées pour accéder aux moitiés 2 32 bits de la valeur entière de type long.</span><span class="sxs-lookup"><span data-stu-id="26fae-161">The **HighPart** and **LowPart** methods are used to access the two 32-bit halves of the large integer value.</span></span>

<span data-ttu-id="26fae-162">Exemple :</span><span class="sxs-lookup"><span data-stu-id="26fae-162">Example:</span></span>


```VB
Dim x as IADsLargeInteger
Set o = GetObject("LDAP://DC=Fabrikam,DC=com")
Set x = o.Get("UsnCreated")
Debug.Print x.HighPart
Debug.Print x.LowPart
```



## <a name="octet-string"></a><span data-ttu-id="26fae-163">Chaîne d’octets</span><span class="sxs-lookup"><span data-stu-id="26fae-163">Octet String</span></span>


```VB
Syntax Type: ADSTYPE_OCTET_STRING
```



<span data-ttu-id="26fae-164">Une chaîne d’octets est retournée en tant que tableau variant d’octets.</span><span class="sxs-lookup"><span data-stu-id="26fae-164">An octet string is returned as a variant array of bytes.</span></span> <span data-ttu-id="26fae-165">Cela se compose d’un nombre de tailles (nombre d’octets) suivi d’une série d’octets.</span><span class="sxs-lookup"><span data-stu-id="26fae-165">This consists of a size count (number of octets) followed by a series of octets.</span></span> <span data-ttu-id="26fae-166">Un octet est un octet de 8 bits, de sorte qu’une série d’octets est une chaîne de données binaires.</span><span class="sxs-lookup"><span data-stu-id="26fae-166">An octet is an 8-bit byte, so a series of octets is a string of binary data.</span></span>

## <a name="object-class"></a><span data-ttu-id="26fae-167">Classe d’objet</span><span class="sxs-lookup"><span data-stu-id="26fae-167">Object Class</span></span>


```VB
Syntax Type: ADSTYPE_CASE_IGNORE_STRING
```



<span data-ttu-id="26fae-168">La classe Object est un identificateur d’objet unique pour une classe de schéma donnée.</span><span class="sxs-lookup"><span data-stu-id="26fae-168">Object Class is a unique object identifier for a given schema class.</span></span> <span data-ttu-id="26fae-169">La classe de chaque instance d’objet est identifiée par l’attribut **objectClass** .</span><span class="sxs-lookup"><span data-stu-id="26fae-169">The class of each object instance is identified by the **objectClass** attribute.</span></span> <span data-ttu-id="26fae-170">Une fois créée, vous ne pouvez jamais modifier une classe d’objet.</span><span class="sxs-lookup"><span data-stu-id="26fae-170">When created, you can never change an object class.</span></span> <span data-ttu-id="26fae-171">**objectClass** est un attribut à valeurs multiples.</span><span class="sxs-lookup"><span data-stu-id="26fae-171">**objectClass** is a multiple valued attribute.</span></span> <span data-ttu-id="26fae-172">Elle répertorie la classe spécifique de l’objet, ainsi que les classes de toutes les classes structurelles ou abstraites à partir desquelles la classe spécifique a été dérivée.</span><span class="sxs-lookup"><span data-stu-id="26fae-172">It lists the specific class of the object, and the classes of all structural or abstract classes from which the specific class was derived.</span></span> <span data-ttu-id="26fae-173">Cela comprend top, la classe à partir de laquelle toutes les autres classes sont dérivées en fin de compte.</span><span class="sxs-lookup"><span data-stu-id="26fae-173">This includes Top, the class from which all other classes are ultimately derived.</span></span> <span data-ttu-id="26fae-174">Active Directory ne répertorie pas les classes auxiliaires dans l’attribut **objectClass** .</span><span class="sxs-lookup"><span data-stu-id="26fae-174">Active Directory does not list auxiliary classes in the **objectClass** attribute.</span></span>

## <a name="security-descriptor"></a><span data-ttu-id="26fae-175">Descripteur de sécurité</span><span class="sxs-lookup"><span data-stu-id="26fae-175">Security Descriptor</span></span>


```VB
Syntax Type: ADSTYPE_NT_SECURITY_DESCRIPTOR
```



<span data-ttu-id="26fae-176">Les droits d’accès définissent les capacités d’un principal de sécurité lorsqu’il tente d’effectuer une opération sur un objet Active Directory.</span><span class="sxs-lookup"><span data-stu-id="26fae-176">Access rights define what abilities a security principal has when it attempts to perform an operation on an Active Directory object.</span></span> <span data-ttu-id="26fae-177">Un descripteur de sécurité décrit les informations de contrôle d’accès associées à un objet.</span><span class="sxs-lookup"><span data-stu-id="26fae-177">A security descriptor describes the access control information associated with an object.</span></span>

<span data-ttu-id="26fae-178">Le descripteur de sécurité est stocké en tant que propriété d’un objet d’annuaire dans la propriété **ntSecurityDescriptor** .</span><span class="sxs-lookup"><span data-stu-id="26fae-178">The security descriptor is stored as a property of a directory object in the **nTSecurityDescriptor** property.</span></span> <span data-ttu-id="26fae-179">Lorsqu’un utilisateur authentifié tente d’accéder à un objet d’annuaire, le serveur d’annuaire détermine l’accès accordé ou refusé à l’utilisateur en fonction du descripteur de sécurité de l’objet.</span><span class="sxs-lookup"><span data-stu-id="26fae-179">When an authenticated user attempts to access a directory object, the directory server determines the access granted or denied to the user based on the object security descriptor.</span></span>

<span data-ttu-id="26fae-180">L’énumération [**\_ \_ \_ enum du contrôle SD ADS**](/windows/win32/api/iads/ne-iads-ads_sd_control_enum) spécifie des indicateurs de contrôle pour un descripteur de sécurité.</span><span class="sxs-lookup"><span data-stu-id="26fae-180">The [**ADS\_SD\_CONTROL\_ENUM**](/windows/win32/api/iads/ne-iads-ads_sd_control_enum) enumeration specifies control flags for a security descriptor.</span></span>

<span data-ttu-id="26fae-181">L’exemple de code suivant montre comment obtenir un descripteur de sécurité.</span><span class="sxs-lookup"><span data-stu-id="26fae-181">The following code example shows how to obtain a security descriptor.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="26fae-182">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="26fae-182">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="26fae-183">Syntaxes pour les attributs Active Directory</span><span class="sxs-lookup"><span data-stu-id="26fae-183">Syntaxes for Active Directory Attributes</span></span>](/windows/desktop/AD/syntaxes-for-attributes-in-active-directory-domain-services)
</dt> <dt>

[<span data-ttu-id="26fae-184">Choix d’une syntaxe</span><span class="sxs-lookup"><span data-stu-id="26fae-184">Choosing a Syntax</span></span>](/windows/desktop/AD/choosing-a-syntax)
</dt> <dt>

[<span data-ttu-id="26fae-185">Comment spécifier des valeurs de comparaison</span><span class="sxs-lookup"><span data-stu-id="26fae-185">How to Specify Comparison Values</span></span>](/windows/desktop/AD/how-to-specify-comparison-values)
</dt> </dl>

 

 