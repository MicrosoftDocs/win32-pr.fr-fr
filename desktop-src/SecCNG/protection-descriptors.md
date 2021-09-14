---
description: Une chaîne de règle de descripteur de protection contient une liste séquentielle d’un ou de plusieurs protecteurs.
ms.assetid: FBFE2143-DC40-40F3-83CE-E6D8841F9C11
title: Descripteurs de protection
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11814df2af5bd9abee4260f4aadab5bb74c77a9f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127013655"
---
# <a name="protection-descriptors"></a>Descripteurs de protection

Une chaîne de règle de descripteur de protection contient une liste séquentielle d’un ou de plusieurs protecteurs. Il doit y avoir au moins un protecteur. S’il en existe plusieurs, les protecteurs doivent être séparés dans la chaîne par **and** ou **or**. Ces valeurs doivent être en majuscules. La syntaxe suivante illustre le format de chaîne d’un descripteur de protection.


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



Les descripteurs de protection peuvent actuellement être définis pour les types d’autorisation suivants :

-   Groupe dans une forêt Active Directory.
-   Ensemble d’informations d’identification Web.
-   Un certificat dans le magasin de certificats de l’utilisateur.

Voici des exemples de chaînes de règles de descripteur de protection pour un groupe de Active Directory :

-   « SID = S-1-5-21-4392301 ET SID = S-1-5-21-3101812 »
-   "SDDL = O :S-1-5-5-0-290724G : SYD : (A ;; CCDC;;; S-1-5-5-0-290724) (A ;;D C ;;; WD)»
-   « LOCAL = utilisateur »
-   « LOCAL = machine »

Voici des exemples de chaînes de règles de descripteur de protection pour un ensemble d’informations d’identification Web :

-   « Webinformations = MyPasswordName »
-   « Webinformations = MyPasswordName, mon_site_Web. com »

Voici des exemples de chaînes de règles de descripteur de protection pour un certificat :

-   « CERTIFICATe = HashID : \_ hachage SHA1 \_ du \_ certificat »
-   « CERTIFICATe = CertBlob : base64String »

Le descripteur de protection que vous spécifiez détermine automatiquement le fournisseur de protection de clés utilisé. Pour plus d’informations, consultez [fournisseurs de protection](protection-providers.md).

Notez que le côté gauche du signe égal (=) doit être un **sid**, un **SDDL**, un **local**, des **informations d’identification** ou un **certificat**. Ces valeurs ne respectent pas la casse.

Vous devez spécifier une chaîne de règle (ou un nom d’affichage associé à une chaîne de règle) lorsque vous appelez la fonction [**NCryptCreateProtectionDescriptor**](/windows/desktop/api/NCryptprotect/nf-ncryptprotect-ncryptcreateprotectiondescriptor) . En guise d’alternative, comme les chaînes de règle du descripteur de protection sont peu encombrantes à utiliser et à mémoriser, vous pouvez associer un nom complet à la chaîne de règle et inscrire les deux à l’aide de la fonction [**NCryptRegisterProtectionDescriptorName**](/windows/desktop/api/NCryptprotect/nf-ncryptprotect-ncryptregisterprotectiondescriptorname) . Vous pouvez ensuite utiliser le nom d’affichage dans **NCryptCreateProtectionDescriptor**.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[DPAPI CNG](cng-dpapi.md)
</dt> <dt>

[Fournisseurs de protection](protection-providers.md)
</dt> </dl>

 

 



