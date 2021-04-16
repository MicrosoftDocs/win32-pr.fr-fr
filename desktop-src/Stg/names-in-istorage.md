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
# <a name="names-in-istorage"></a>Noms dans IStorage

Un jeu de propriétés est identifié par un identificateur de format (FMTID) dans l’interface [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) . Dans l’interface [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) , un jeu de propriétés est nommé avec une chaîne Unicode se terminant par un caractère NULL avec une longueur maximale de 32 caractères. Pour activer l’interopérabilité, un mappage entre un FMTID et une chaîne Unicode correspondante se terminant par un caractère null doit être établi.

## <a name="converting-a-property-set-from-a-fmtid-to-a-string-name"></a>Conversion d’un jeu de propriétés d’un FMTID en nom de chaîne

Lors de la conversion d’un FMTID en nom de chaîne Unicode correspondant, vérifiez d’abord que le FMTID est une valeur connue, répertoriée dans le tableau suivant. Si c’est le cas, utilisez le nom de chaîne connu correspondant.

| FMTID                                                                                | Nom de la chaîne                       | Équivalent                                                         |
|--------------------------------------------------------------------------------------|-----------------------------------|------------------------------------------------------------------|
| F29F85E0-4FF9-1068-AB91-08002B27B3D9                                                 | « \\ 005SummaryInformation »         | Informations résumées sur le COM2                                         |
| D5CDD502-2E9C-101B-9397-08002B2CF9AE D5CDD505-2E9C-101B-9397-08002B2CF9AE<br/> | « \\ 005DocumentSummaryInformation » | Informations récapitulatives sur les documents Office et propriétés définies par l’utilisateur. |



 

> [!Note]  
> La propriété **DocumentSummaryInformation** et **UserDefined** définie est unique, car elle contient deux sections. Plusieurs sections ne sont pas autorisées dans un autre jeu de propriétés. Pour plus d’informations, consultez [format du jeu de propriétés sérialisées de stockage structuré](structured-storage-serialized-property-set-format.md), ainsi que [les jeux de propriétés DocumentSummaryInformation et UserDefined](the-documentsummaryinformation-and-userdefined-property-sets.md). La première section a été définie dans le cadre de COM ; la seconde a été définie par Microsoft Office.

 

Si FMTID n’est pas une valeur connue, utilisez la procédure suivante pour former algorithmiquement un nom de chaîne.

**Pour former algorithmiquement un nom de chaîne**

1.  Convertissez le FMTID en ordre d’octet Little-endian, si nécessaire.
2.  Prenez les 128 bits du FMTID et considérez-les comme une chaîne de bits longue en concaténant chacun des octets ensemble. Le premier bit de la valeur 128 bit est le bit le moins significatif du premier octet de la mémoire du FMTID. le dernier bit de la valeur 128 bit est le bit le plus significatif du dernier octet de la mémoire du FMTID. Étendez ces 128 bits à 130 bits en ajoutant deux bits nuls à la fin.
3.  Divisez les bits 130 en groupes de cinq bits ; Il y aura 26 groupes de ce type. Considérez chaque groupe comme un entier avec une priorité de bit inversée. Par exemple, le premier des 128 bits est le bit le moins significatif du premier groupe de cinq bits ; le cinquième des 128 bits est le bit le plus significatif du premier groupe.
4.  Mappez chacun de ces entiers en tant qu’index dans le tableau de 32 caractères : ABCDEFGHIJKLMNOPQRSTUVWXYZ012345. Cela génère une séquence de 26 caractères Unicode qui utilise uniquement des caractères majuscules et des chiffres. Les considérations sensibles à la casse et ne respectant pas la casse ne s’appliquent pas, ce qui amène chaque caractère à être unique dans tous les paramètres régionaux.
5.  Créez la chaîne finale en concaténant la chaîne « \\ 005 » sur le début de ces 26 caractères, pour une longueur totale de 27 caractères.

L’exemple de code suivant montre comment mapper un FMTID à une chaîne de propriété.


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



## <a name="converting-a-property-set-from-a-string-name-to-a-fmtid"></a>Conversion d’un jeu de propriétés d’un nom de chaîne en FMTID

Les convertisseurs de noms de chaîne de propriété en GUID doivent accepter des minuscules comme synonymes de leurs équivalents majuscules.

L’exemple de code suivant montre comment mapper une chaîne de propriété à un FMTID.


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



Lorsque vous tentez d’ouvrir un jeu de propriétés existant, dans [IPropertySetStorage :: Open](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-open), le fmtid (racine) est converti en chaîne comme décrit ci-dessus. Si un élément de l' [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) de ce nom existe, il est utilisé. Dans le cas contraire, l’ouverture échoue.

Lorsque vous créez un nouveau jeu de propriétés, le mappage ci-dessus détermine le nom de chaîne utilisé.

 

 





