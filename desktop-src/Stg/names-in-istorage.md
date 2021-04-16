---
title: Noms dans IStorage
description: Un jeu de propriétés est identifié par un identificateur de format (FMTID) dans l’interface IPropertySetStorage.
ms.assetid: 5f8eba37-c589-413e-9971-7ecb01dc6734
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6cef9417f2f5fad7fd17dcc3d431f1d3565a3843
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104507463"
---
# <a name="names-in-istorage"></a><span data-ttu-id="bfd6b-103">Noms dans IStorage</span><span class="sxs-lookup"><span data-stu-id="bfd6b-103">Names in IStorage</span></span>

<span data-ttu-id="bfd6b-104">Un jeu de propriétés est identifié par un identificateur de format (FMTID) dans l’interface [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) .</span><span class="sxs-lookup"><span data-stu-id="bfd6b-104">A property set is identified with a format identifier (FMTID) in the [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) interface.</span></span> <span data-ttu-id="bfd6b-105">Dans l’interface [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) , un jeu de propriétés est nommé avec une chaîne Unicode se terminant par un caractère NULL avec une longueur maximale de 32 caractères.</span><span class="sxs-lookup"><span data-stu-id="bfd6b-105">In the [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) interface, a property set is named with a null-terminated Unicode string with a maximum length of 32 characters.</span></span> <span data-ttu-id="bfd6b-106">Pour activer l’interopérabilité, un mappage entre un FMTID et une chaîne Unicode correspondante se terminant par un caractère null doit être établi.</span><span class="sxs-lookup"><span data-stu-id="bfd6b-106">To enable interoperability, a mapping between an FMTID and a corresponding null-terminated Unicode string must be established.</span></span>

## <a name="converting-a-property-set-from-a-fmtid-to-a-string-name"></a><span data-ttu-id="bfd6b-107">Conversion d’un jeu de propriétés d’un FMTID en nom de chaîne</span><span class="sxs-lookup"><span data-stu-id="bfd6b-107">Converting a property set from a FMTID to a string name</span></span>

<span data-ttu-id="bfd6b-108">Lors de la conversion d’un FMTID en nom de chaîne Unicode correspondant, vérifiez d’abord que le FMTID est une valeur connue, répertoriée dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="bfd6b-108">When converting from an FMTID to a corresponding Unicode string name, first verify that the FMTID is a well-known value, listed in the following table.</span></span> <span data-ttu-id="bfd6b-109">Si c’est le cas, utilisez le nom de chaîne connu correspondant.</span><span class="sxs-lookup"><span data-stu-id="bfd6b-109">If so, then use the corresponding well-known string name.</span></span>

| <span data-ttu-id="bfd6b-110">FMTID</span><span class="sxs-lookup"><span data-stu-id="bfd6b-110">FMTID</span></span>                                                                                | <span data-ttu-id="bfd6b-111">Nom de la chaîne</span><span class="sxs-lookup"><span data-stu-id="bfd6b-111">String name</span></span>                       | <span data-ttu-id="bfd6b-112">Équivalent</span><span class="sxs-lookup"><span data-stu-id="bfd6b-112">Semantic</span></span>                                                         |
|--------------------------------------------------------------------------------------|-----------------------------------|------------------------------------------------------------------|
| <span data-ttu-id="bfd6b-113">F29F85E0-4FF9-1068-AB91-08002B27B3D9</span><span class="sxs-lookup"><span data-stu-id="bfd6b-113">F29F85E0-4FF9-1068-AB91-08002B27B3D9</span></span>                                                 | <span data-ttu-id="bfd6b-114">« \\ 005SummaryInformation »</span><span class="sxs-lookup"><span data-stu-id="bfd6b-114">"\\005SummaryInformation"</span></span>         | <span data-ttu-id="bfd6b-115">Informations résumées sur le COM2</span><span class="sxs-lookup"><span data-stu-id="bfd6b-115">COM2 summary information</span></span>                                         |
| <span data-ttu-id="bfd6b-116">D5CDD502-2E9C-101B-9397-08002B2CF9AE D5CDD505-2E9C-101B-9397-08002B2CF9AE</span><span class="sxs-lookup"><span data-stu-id="bfd6b-116">D5CDD502-2E9C-101B-9397-08002B2CF9AE D5CDD505-2E9C-101B-9397-08002B2CF9AE</span></span><br/> | <span data-ttu-id="bfd6b-117">« \\ 005DocumentSummaryInformation »</span><span class="sxs-lookup"><span data-stu-id="bfd6b-117">"\\005DocumentSummaryInformation"</span></span> | <span data-ttu-id="bfd6b-118">Informations récapitulatives sur les documents Office et propriétés définies par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="bfd6b-118">Office document summary information and user-defined properties.</span></span> |



 

> [!Note]  
> <span data-ttu-id="bfd6b-119">La propriété **DocumentSummaryInformation** et **UserDefined** définie est unique, car elle contient deux sections.</span><span class="sxs-lookup"><span data-stu-id="bfd6b-119">The **DocumentSummaryInformation** and **UserDefined** property set is unique in that it contains two sections.</span></span> <span data-ttu-id="bfd6b-120">Plusieurs sections ne sont pas autorisées dans un autre jeu de propriétés.</span><span class="sxs-lookup"><span data-stu-id="bfd6b-120">Multiple sections are not permitted in any other property set.</span></span> <span data-ttu-id="bfd6b-121">Pour plus d’informations, consultez [format du jeu de propriétés sérialisées de stockage structuré](structured-storage-serialized-property-set-format.md), ainsi que [les jeux de propriétés DocumentSummaryInformation et UserDefined](the-documentsummaryinformation-and-userdefined-property-sets.md).</span><span class="sxs-lookup"><span data-stu-id="bfd6b-121">For more information, see [Structured Storage Serialized Property Set Format](structured-storage-serialized-property-set-format.md), and [The DocumentSummaryInformation and UserDefined Property Sets](the-documentsummaryinformation-and-userdefined-property-sets.md).</span></span> <span data-ttu-id="bfd6b-122">La première section a été définie dans le cadre de COM ; la seconde a été définie par Microsoft Office.</span><span class="sxs-lookup"><span data-stu-id="bfd6b-122">The first section was defined as part of COM; the second was defined by Microsoft Office.</span></span>

 

<span data-ttu-id="bfd6b-123">Si FMTID n’est pas une valeur connue, utilisez la procédure suivante pour former algorithmiquement un nom de chaîne.</span><span class="sxs-lookup"><span data-stu-id="bfd6b-123">If the FMTID is not a well-known value, then use the following procedure to algorithmically form a string name.</span></span>

<span data-ttu-id="bfd6b-124">**Pour former algorithmiquement un nom de chaîne**</span><span class="sxs-lookup"><span data-stu-id="bfd6b-124">**To algorithmically form a string name**</span></span>

1.  <span data-ttu-id="bfd6b-125">Convertissez le FMTID en ordre d’octet Little-endian, si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="bfd6b-125">Convert the FMTID to little-endian byte order, if necessary.</span></span>
2.  <span data-ttu-id="bfd6b-126">Prenez les 128 bits du FMTID et considérez-les comme une chaîne de bits longue en concaténant chacun des octets ensemble.</span><span class="sxs-lookup"><span data-stu-id="bfd6b-126">Take the 128 bits of the FMTID and consider them as one long bit string by concatenating each of the bytes together.</span></span> <span data-ttu-id="bfd6b-127">Le premier bit de la valeur 128 bit est le bit le moins significatif du premier octet de la mémoire du FMTID. le dernier bit de la valeur 128 bit est le bit le plus significatif du dernier octet de la mémoire du FMTID.</span><span class="sxs-lookup"><span data-stu-id="bfd6b-127">The first bit of the 128 bit value is the least significant bit of the first byte in memory of the FMTID; the last bit of the 128 bit value is the most significant bit of the last byte in memory of the FMTID.</span></span> <span data-ttu-id="bfd6b-128">Étendez ces 128 bits à 130 bits en ajoutant deux bits nuls à la fin.</span><span class="sxs-lookup"><span data-stu-id="bfd6b-128">Extend these 128 bits to 130 bits by adding two zero bits to the end.</span></span>
3.  <span data-ttu-id="bfd6b-129">Divisez les bits 130 en groupes de cinq bits ; Il y aura 26 groupes de ce type.</span><span class="sxs-lookup"><span data-stu-id="bfd6b-129">Divide the 130 bits into groups of five bits; there will be 26 such groups.</span></span> <span data-ttu-id="bfd6b-130">Considérez chaque groupe comme un entier avec une priorité de bit inversée.</span><span class="sxs-lookup"><span data-stu-id="bfd6b-130">Consider each group as an integer with reversed bit precedence.</span></span> <span data-ttu-id="bfd6b-131">Par exemple, le premier des 128 bits est le bit le moins significatif du premier groupe de cinq bits ; le cinquième des 128 bits est le bit le plus significatif du premier groupe.</span><span class="sxs-lookup"><span data-stu-id="bfd6b-131">For example, the first of the 128 bits is the least significant bit of the first group of five bits; the fifth of the 128 bits is the most significant bit of the first group.</span></span>
4.  <span data-ttu-id="bfd6b-132">Mappez chacun de ces entiers en tant qu’index dans le tableau de 32 caractères : ABCDEFGHIJKLMNOPQRSTUVWXYZ012345.</span><span class="sxs-lookup"><span data-stu-id="bfd6b-132">Map each of these integers as an index into the array of thirty-two characters: ABCDEFGHIJKLMNOPQRSTUVWXYZ012345.</span></span> <span data-ttu-id="bfd6b-133">Cela génère une séquence de 26 caractères Unicode qui utilise uniquement des caractères majuscules et des chiffres.</span><span class="sxs-lookup"><span data-stu-id="bfd6b-133">This yields a sequence of 26 Unicode characters that uses only uppercase characters and numerals.</span></span> <span data-ttu-id="bfd6b-134">Les considérations sensibles à la casse et ne respectant pas la casse ne s’appliquent pas, ce qui amène chaque caractère à être unique dans tous les paramètres régionaux.</span><span class="sxs-lookup"><span data-stu-id="bfd6b-134">Case sensitive and case insensitive considerations do not apply, causing each character to be unique in any locale.</span></span>
5.  <span data-ttu-id="bfd6b-135">Créez la chaîne finale en concaténant la chaîne « \\ 005 » sur le début de ces 26 caractères, pour une longueur totale de 27 caractères.</span><span class="sxs-lookup"><span data-stu-id="bfd6b-135">Create the final string by concatenating the string "\\005" onto the front of these 26 characters, for a total length of 27 characters.</span></span>

<span data-ttu-id="bfd6b-136">L’exemple de code suivant montre comment mapper un FMTID à une chaîne de propriété.</span><span class="sxs-lookup"><span data-stu-id="bfd6b-136">The following example code shows how to map from an FMTID to a property string.</span></span>


```C++
#define CBIT_BYTE        8
#define CBIT_CHARMASK    5
#define CCH_MAP          (1 << CBIT_CHARMASK)    // 32
#define CHARMASK         (CCH_MAP - 1)           // 0x1f
 
CHAR awcMap[CCH_MAP + 1] = "abcdefghijklmnopqrstuvwxyz012345";
 
WCHAR MapChar(ULONG I) {
    return((WCHAR) awcMap[i & CHARMASK]);
    }
 
VOID GuidToPropertyStringName(GUID *pguid, WCHAR awcname[]) {
    BYTE *pb = (BYTE *) pguid;
    BYTE *pbEnd = pb + sizeof(*pguid);
    ULONG cbitRemain = CBIT_BYTE;
    WCHAR *pwc = awcname;
 
    *pwc++ = ((WCHAR) 0x0005);
    while (pb < pbEnd) {
        ULONG i = *pb >> (CBIT_BYTE - cbitRemain);
        if (cbitRemain >= CBIT_CHARMASK) {
            *pwc = MapChar(i);
            if (cbitRemain == CBIT_BYTE && 
                                    *pwc >= L'a' && *pwc <= L'z')
                {
                *pwc += (WCHAR) (L'A' - L'a');
                }
            pwc++;
            cbitRemain -= CBIT_CHARMASK;
            if (cbitRemain == 0) {
                pb++;
                cbitRemain = CBIT_BYTE;
                }
            }
        else {
            if (++pb < pbEnd) {
                i |= *pb << cbitRemain;
                }
            *pwc++ = MapChar(i);
            cbitRemain += CBIT_BYTE - CBIT_CHARMASK;
            }
        }
    *pwc = L'\0';
    }
```



## <a name="converting-a-property-set-from-a-string-name-to-a-fmtid"></a><span data-ttu-id="bfd6b-137">Conversion d’un jeu de propriétés d’un nom de chaîne en FMTID</span><span class="sxs-lookup"><span data-stu-id="bfd6b-137">Converting a property set from a string name to a FMTID</span></span>

<span data-ttu-id="bfd6b-138">Les convertisseurs de noms de chaîne de propriété en GUID doivent accepter des minuscules comme synonymes de leurs équivalents majuscules.</span><span class="sxs-lookup"><span data-stu-id="bfd6b-138">Converters of property string names to GUIDs should accept lowercase letters as synonymous with their uppercase counterparts.</span></span>

<span data-ttu-id="bfd6b-139">L’exemple de code suivant montre comment mapper une chaîne de propriété à un FMTID.</span><span class="sxs-lookup"><span data-stu-id="bfd6b-139">The following example code shows how to map from a property string to an FMTID.</span></span>


```C++
#include "stdafx.h"
#define _INC_OLE
#include <windows.h>
#include <stdlib.h>
#include <stdio.h>
#include <string.h>
#include <ctype.h>
#define CBIT_CHARMASK 5
#define CBIT_BYTE     8
#define CBIT_GUID    (CBIT_BYTE * sizeof(GUID))
#define CWC_PROPSET  (1 + (CBIT_GUID + CBIT_CHARMASK-1)/CBIT_CHARMASK)
#define WC_PROPSET0  ((WCHAR) 0x0005)
#define CCH_MAP      (1 << CBIT_CHARMASK)        // 32
#define CHARMASK     (CCH_MAP - 1)            // 0x1f
CHAR awcMap[CCH_MAP + 1] = "abcdefghijklmnopqrstuvwxyz012345";
#define CALPHACHARS  ('z' - 'a' + 1)

GUID guidSummary =
{ 0xf29f85e0,0x4ff9, 0x1068,
{ 0xab, 0x91, 0x08, 0x00, 0x2b, 0x27, 0xb3, 0xd9 } };

WCHAR wszSummary[] = L"SummaryInformation";

GUID guidDocumentSummary =
    { 0xd5cdd502,
      0x2e9c, 0x101b,
      { 0x93, 0x97, 0x08, 0x00, 0x2b, 0x2c, 0xf9, 0xae } };

WCHAR wszDocumentSummary[] = L"DocumentSummaryInformation";
__inline WCHAR

MapChar(IN ULONG i)
{
    return((WCHAR) awcMap[i & CHARMASK]);
}

ULONG PropertySetNameToGuid(
    IN ULONG cwcname,
    IN WCHAR const awcname[],
    OUT GUID *pguid)
{
    ULONG Status = ERROR_INVALID_PARAMETER;
    WCHAR const *pwc = awcname;

    if (pwc[0] == WC_PROPSET0)
    {
        //Note: cwcname includes the WC_PROPSET0, and
        //sizeof(wsz...) includes the trailing L'\0', but
        //the comparison excludes both the leading
        //WC_PROPSET0 and the trailing L'\0'.
        if (cwcname == sizeof(wszSummary)/sizeof(WCHAR) &&
            wcsnicmp(&pwc[1], wszSummary, cwcname - 1) == 0)
        {
            *pguid = guidSummary;
            return(NO_ERROR);
        }
        if (cwcname == CWC_PROPSET)
        {
            ULONG cbit;
            BYTE *pb = (BYTE *) pguid - 1;
            ZeroMemory(pguid, sizeof(*pguid));
            for (cbit = 0; cbit < CBIT_GUID; cbit += 
            CBIT_CHARMASK)
            {
                ULONG cbitUsed = cbit % CBIT_BYTE;
                ULONG cbitStored;
                WCHAR wc;
                if (cbitUsed == 0)
                {
                    pb++;
                }
                wc = *++pwc - L'A';        //assume uppercase
                if (wc > CALPHACHARS)
                {
                    wc += (WCHAR) (L'A' - L'a'); //try lowercase
                    if (wc > CALPHACHARS)
                    {
                        wc += L'a' - L'0' + CALPHACHARS; 
                        if (wc > CHARMASK)
                        {
                            goto fail;       //invalid character
                        }
                    }
                }
                *pb |= (BYTE) (wc << cbitUsed);
                cbitStored = min(CBIT_BYTE - cbitUsed, 
                CBIT_CHARMASK);

                //If the translated bits will not fit in the 
                //current byte
                if (cbitStored < CBIT_CHARMASK)
                {
                    wc >>= CBIT_BYTE - cbitUsed;
                    if (cbit + cbitStored == CBIT_GUID)
                    {
                       if (wc != 0)
                       {
                           goto fail;        //extra bits
                       }
                       break;
                    }
                    pb++;
                    *pb |= (BYTE) wc;
                }
           }
           Status = NO_ERROR;
      }
    }
fail:
    return(Status);
}
```



<span data-ttu-id="bfd6b-140">Lorsque vous tentez d’ouvrir un jeu de propriétés existant, dans [IPropertySetStorage :: Open](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-open), le fmtid (racine) est converti en chaîne comme décrit ci-dessus.</span><span class="sxs-lookup"><span data-stu-id="bfd6b-140">When attempting to open an existing property set, in [IPropertySetStorage::Open](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-open), the (root) FMTID is converted to a string as described above.</span></span> <span data-ttu-id="bfd6b-141">Si un élément de l' [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) de ce nom existe, il est utilisé.</span><span class="sxs-lookup"><span data-stu-id="bfd6b-141">If an element of the [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) of that name exists, it is used.</span></span> <span data-ttu-id="bfd6b-142">Dans le cas contraire, l’ouverture échoue.</span><span class="sxs-lookup"><span data-stu-id="bfd6b-142">Otherwise, the open fails.</span></span>

<span data-ttu-id="bfd6b-143">Lorsque vous créez un nouveau jeu de propriétés, le mappage ci-dessus détermine le nom de chaîne utilisé.</span><span class="sxs-lookup"><span data-stu-id="bfd6b-143">When creating a new property set, the above mapping determines the string name used.</span></span>

 

 





