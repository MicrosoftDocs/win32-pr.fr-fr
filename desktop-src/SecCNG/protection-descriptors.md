---
description: Une chaîne de règle de descripteur de protection contient une liste séquentielle d’un ou de plusieurs protecteurs.
ms.assetid: FBFE2143-DC40-40F3-83CE-E6D8841F9C11
title: Descripteurs de protection
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11814df2af5bd9abee4260f4aadab5bb74c77a9f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104202394"
---
# <a name="protection-descriptors"></a><span data-ttu-id="afd20-103">Descripteurs de protection</span><span class="sxs-lookup"><span data-stu-id="afd20-103">Protection Descriptors</span></span>

<span data-ttu-id="afd20-104">Une chaîne de règle de descripteur de protection contient une liste séquentielle d’un ou de plusieurs protecteurs.</span><span class="sxs-lookup"><span data-stu-id="afd20-104">A protection descriptor rule string contains a sequential list of one or more protectors.</span></span> <span data-ttu-id="afd20-105">Il doit y avoir au moins un protecteur.</span><span class="sxs-lookup"><span data-stu-id="afd20-105">There must be at least one protector.</span></span> <span data-ttu-id="afd20-106">S’il en existe plusieurs, les protecteurs doivent être séparés dans la chaîne par **and** ou **or**.</span><span class="sxs-lookup"><span data-stu-id="afd20-106">If there is more than one, the protectors must be separated in the string by **AND** or **OR**.</span></span> <span data-ttu-id="afd20-107">Ces valeurs doivent être en majuscules.</span><span class="sxs-lookup"><span data-stu-id="afd20-107">These values must be capitalized.</span></span> <span data-ttu-id="afd20-108">La syntaxe suivante illustre le format de chaîne d’un descripteur de protection.</span><span class="sxs-lookup"><span data-stu-id="afd20-108">The following syntax shows the string format of a protection descriptor.</span></span>


```C++
Descriptor = [ Protector-or
              *( OR-separator Protector-or ) ]

    Protector-or = Protector-and
              *( AND-separator Protector-and )

    OR-separator = "OR"
    AND-separator = "AND"

    Protector-and = providerName EQUALS providerAttributes

    providerName = descr

    providerAttribute = string | hexstring

      ; The following characters are to be escaped when they appear
      ; in the value to be encoded: ESC, one of <escaped>, leading
      ; SHARP or SPACE, trailing SPACE, and NULL.
      string =   [ ( leadchar / pair ) [ *( stringchar / pair )
         ( trailchar / pair ) ] ]

      leadchar = LUTF1 / UTFMB
      LUTF1 = %x01-1F / %x21 / %x24-2A / %x2D-3A / %x3D / %x3F-5B / %x5D-7F

      trailchar  = TUTF1 / UTFMB
      TUTF1 = %x01-1F / %x21 / %x23-2A / %x2D-3A / %x3D / %x3F-5B / %x5D-7F

      stringchar = SUTF1 / UTFMB
      SUTF1 = %x01-21 / %x23-2A / %x2D-3A / %x3D / %x3F-5B / %x5D-7F

      pair = ESC ( ESC / special / hexpair )
      special = escaped / SPACE / SHARP / EQUALS
      escaped = DQUOTE / PLUS / COMMA / SEMI / LANGLE / RANGLE
      hexstring = SHARP 1*hexpair
      hexpair = HEX HEX

      descr   = leadkeychar *keychar
      leadkeychar = ALPHA
      keychar = ALPHA / DIGIT / HYPHEN
      number  = DIGIT / ( LDIGIT 1*DIGIT )

      ALPHA   = %x41-5A / %x61-7A   ; "A"-"Z" / "a"-"z"
      DIGIT   = %x30 / LDIGIT       ; "0"-"9"
      LDIGIT  = %x31-39             ; "1"-"9"
      HEX     = DIGIT / %x41-46 / %x61-66 ; "0"-"9" / "A"-"F" / "a"-"f"

      NULL    = %x00 ; null (0)
      SPACE   = %x20 ; space (" ")
      DQUOTE  = %x22 ; quote (""")
      SHARP   = %x23 ; octothorpe (or sharp sign) ("#")
      DOLLAR  = %x24 ; dollar sign ("$")
      SQUOTE  = %x27 ; single quote ("'")
      LPAREN  = %x28 ; left paren ("(")
      RPAREN  = %x29 ; right paren (")")
      PLUS    = %x2B ; plus sign ("+")
      COMMA   = %x2C ; comma (",")
      HYPHEN  = %x2D ; hyphen ("-")
      DOT     = %x2E ; period (".")
      SEMI    = %x3B ; semicolon (";")
      LANGLE  = %x3C ; left angle bracket ("<")
      EQUALS  = %x3D ; equals sign ("=")
      RANGLE  = %x3E ; right angle bracket (">")
      ESC     = %x5C ; backslash ("\")
      USCORE  = %x5F ; underscore ("_")
      LCURLY  = %x7B ; left curly brace "{"
      RCURLY  = %x7D ; right curly brace "}"

      ; Any UTF-8 [RFC3629] encoded Unicode [Unicode] character
      UTF8    = UTF1 / UTFMB
      UTFMB   = UTF2 / UTF3 / UTF4
      UTF0    = %x80-BF
      UTF1    = %x00-7F
      UTF2    = %xC2-DF UTF0
      UTF3    = %xE0 %xA0-BF UTF0 / %xE1-EC 2(UTF0) /
                %xED %x80-9F UTF0 / %xEE-EF 2(UTF0)
      UTF4    = %xF0 %x90-BF 2(UTF0) / %xF1-F3 3(UTF0) /
                %xF4 %x80-8F 2(UTF0)

      OCTET   = %x00-FF ; Any octet (8-bit data unit)
```



<span data-ttu-id="afd20-109">Les descripteurs de protection peuvent actuellement être définis pour les types d’autorisation suivants :</span><span class="sxs-lookup"><span data-stu-id="afd20-109">Protection descriptors can currently be defined for the following types of authorization:</span></span>

-   <span data-ttu-id="afd20-110">Groupe dans une forêt Active Directory.</span><span class="sxs-lookup"><span data-stu-id="afd20-110">A group in an Active Directory forest.</span></span>
-   <span data-ttu-id="afd20-111">Ensemble d’informations d’identification Web.</span><span class="sxs-lookup"><span data-stu-id="afd20-111">A set of web credentials.</span></span>
-   <span data-ttu-id="afd20-112">Un certificat dans le magasin de certificats de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="afd20-112">A certificate in the user's certificate store.</span></span>

<span data-ttu-id="afd20-113">Voici des exemples de chaînes de règles de descripteur de protection pour un groupe de Active Directory :</span><span class="sxs-lookup"><span data-stu-id="afd20-113">Examples of protection descriptor rule strings for an Active Directory group include the following:</span></span>

-   <span data-ttu-id="afd20-114">« SID = S-1-5-21-4392301 ET SID = S-1-5-21-3101812 »</span><span class="sxs-lookup"><span data-stu-id="afd20-114">"SID=S-1-5-21-4392301 AND SID=S-1-5-21-3101812"</span></span>
-   <span data-ttu-id="afd20-115">"SDDL = O :S-1-5-5-0-290724G : SYD : (A ;; CCDC;;; S-1-5-5-0-290724) (A ;;D C ;;; WD)»</span><span class="sxs-lookup"><span data-stu-id="afd20-115">"SDDL=O:S-1-5-5-0-290724G:SYD:(A;;CCDC;;;S-1-5-5-0-290724)(A;;DC;;;WD)"</span></span>
-   <span data-ttu-id="afd20-116">« LOCAL = utilisateur »</span><span class="sxs-lookup"><span data-stu-id="afd20-116">"LOCAL=user"</span></span>
-   <span data-ttu-id="afd20-117">« LOCAL = machine »</span><span class="sxs-lookup"><span data-stu-id="afd20-117">"LOCAL=machine"</span></span>

<span data-ttu-id="afd20-118">Voici des exemples de chaînes de règles de descripteur de protection pour un ensemble d’informations d’identification Web :</span><span class="sxs-lookup"><span data-stu-id="afd20-118">Examples of protection descriptor rule strings for a set of web credentials include the following:</span></span>

-   <span data-ttu-id="afd20-119">« Webinformations = MyPasswordName »</span><span class="sxs-lookup"><span data-stu-id="afd20-119">"WEBCREDENTIALS=MyPasswordName"</span></span>
-   <span data-ttu-id="afd20-120">« Webinformations = MyPasswordName, mon_site_Web. com »</span><span class="sxs-lookup"><span data-stu-id="afd20-120">"WEBCREDENTIALS=MyPasswordName,myweb.com"</span></span>

<span data-ttu-id="afd20-121">Voici des exemples de chaînes de règles de descripteur de protection pour un certificat :</span><span class="sxs-lookup"><span data-stu-id="afd20-121">Examples of protection descriptor rule strings for a certificate include the following:</span></span>

-   <span data-ttu-id="afd20-122">« CERTIFICATe = HashID : \_ hachage SHA1 \_ du \_ certificat »</span><span class="sxs-lookup"><span data-stu-id="afd20-122">"CERTIFICATE=HashID:sha1\_hash\_of\_certificate"</span></span>
-   <span data-ttu-id="afd20-123">« CERTIFICATe = CertBlob : base64String »</span><span class="sxs-lookup"><span data-stu-id="afd20-123">"CERTIFICATE=CertBlob:base64String"</span></span>

<span data-ttu-id="afd20-124">Le descripteur de protection que vous spécifiez détermine automatiquement le fournisseur de protection de clés utilisé.</span><span class="sxs-lookup"><span data-stu-id="afd20-124">The protection descriptor you specify automatically determines which key protection provider is used.</span></span> <span data-ttu-id="afd20-125">Pour plus d’informations, consultez [fournisseurs de protection](protection-providers.md).</span><span class="sxs-lookup"><span data-stu-id="afd20-125">For more information, see [Protection Providers](protection-providers.md).</span></span>

<span data-ttu-id="afd20-126">Notez que le côté gauche du signe égal (=) doit être un **sid**, un **SDDL**, un **local**, des **informations d’identification** ou un **certificat**.</span><span class="sxs-lookup"><span data-stu-id="afd20-126">Note that the left side of the equals sign (=) must be **SID**, **SDDL**, **LOCAL**, **WEBCREDENTIALS**, or **CERTIFICATE**.</span></span> <span data-ttu-id="afd20-127">Ces valeurs ne respectent pas la casse.</span><span class="sxs-lookup"><span data-stu-id="afd20-127">These values are not case sensitive.</span></span>

<span data-ttu-id="afd20-128">Vous devez spécifier une chaîne de règle (ou un nom d’affichage associé à une chaîne de règle) lorsque vous appelez la fonction [**NCryptCreateProtectionDescriptor**](/windows/desktop/api/NCryptprotect/nf-ncryptprotect-ncryptcreateprotectiondescriptor) .</span><span class="sxs-lookup"><span data-stu-id="afd20-128">You must specify a rule string (or a display name associated with a rule string) when you call the [**NCryptCreateProtectionDescriptor**](/windows/desktop/api/NCryptprotect/nf-ncryptprotect-ncryptcreateprotectiondescriptor) function.</span></span> <span data-ttu-id="afd20-129">En guise d’alternative, comme les chaînes de règle du descripteur de protection sont peu encombrantes à utiliser et à mémoriser, vous pouvez associer un nom complet à la chaîne de règle et inscrire les deux à l’aide de la fonction [**NCryptRegisterProtectionDescriptorName**](/windows/desktop/api/NCryptprotect/nf-ncryptprotect-ncryptregisterprotectiondescriptorname) .</span><span class="sxs-lookup"><span data-stu-id="afd20-129">Alternatively, because protection descriptor rule strings are somewhat cumbersome to use and remember, you can associate a display name with the rule string and register both by using the [**NCryptRegisterProtectionDescriptorName**](/windows/desktop/api/NCryptprotect/nf-ncryptprotect-ncryptregisterprotectiondescriptorname) function.</span></span> <span data-ttu-id="afd20-130">Vous pouvez ensuite utiliser le nom d’affichage dans **NCryptCreateProtectionDescriptor**.</span><span class="sxs-lookup"><span data-stu-id="afd20-130">Then you can use the display name in **NCryptCreateProtectionDescriptor**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="afd20-131">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="afd20-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="afd20-132">DPAPI CNG</span><span class="sxs-lookup"><span data-stu-id="afd20-132">CNG DPAPI</span></span>](cng-dpapi.md)
</dt> <dt>

[<span data-ttu-id="afd20-133">Fournisseurs de protection</span><span class="sxs-lookup"><span data-stu-id="afd20-133">Protection Providers</span></span>](protection-providers.md)
</dt> </dl>

 

 



