---
description: Contient les noms conviviaux des styles SAMI (Synchronized Accessible Media Interchange) définis dans le fichier SAMI.
ms.assetid: bc679f0e-17f6-455c-8a00-1d435538ef86
title: Attribut MF_PD_SAMI_STYLELIST (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ebb07dd1713faa81fd02bfe7a32c81398cddb736
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868546"
---
# <a name="mf_pd_sami_stylelist-attribute"></a>MF \_ PD \_ STYLELIST (attribut same) \_

Contient les noms conviviaux des styles SAMI (Synchronized Accessible Media Interchange) définis dans le fichier SAMI.

La [source du média sami](sami-media-source.md) définit cet attribut sur le descripteur de présentation qu’il crée.

## <a name="data-type"></a>Type de données

Tableau d’octets

## <a name="remarks"></a>Notes

L’objet blob d’attribut a la structure suivante :



Type de données

Description

Taille (en octets)

**GRANDE**

Nombre de chaînes de style.

4

Pour chaque chaîne de style :

**GRANDE**

Taille de la chaîne en octets, y compris le caractère **null** .

4

**LPWSTR**

Chaîne de caractères larges se terminant par un caractère null et contenant le nom du style.

Variable



 

Pour définir le style ou récupérer le style actuel, utilisez l’interface [**IMFSAMIStyle**](/windows/desktop/api/mfidl/nn-mfidl-imfsamistyle) .

La constante GUID de cet attribut est exportée à partir de mfuuid. lib.

## <a name="examples"></a>Exemples


```C++
HRESULT DisplaySAMIStyleNames(IMFPresentationDescriptor *pPD)
{
    UINT8 *pBuf = NULL;
    UINT32 cbBuf = 0;

    HRESULT hr = pPD->GetAllocatedBlob(MF_PD_SAMI_STYLELIST, &pBuf, &cbBuf);

    if (SUCCEEDED(hr))
    {

        DWORD cStyles = ((DWORD*)pBuf)[0];
        UINT8 *pStrings = pBuf + sizeof(DWORD);

        for (DWORD i = 0; i < cStyles; i++)
        {
            DWORD cbString = ((DWORD*)pStrings)[0];
            pStrings += sizeof(DWORD);

            wprintf_s(L"%s\n", (WCHAR*)pStrings);

            pStrings += cbString;
        }
    }
    CoTaskMemFree(pBuf);
    return hr;
}
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                     |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                               |
| En-tête<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Liste alphabétique des attributs Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**IMFAttributes :: GetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[**IMFAttributes :: SetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> <dt>

[**IMFPresentationDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[Attributs du descripteur de présentation](presentation-descriptor-attributes.md)
</dt> <dt>

[Source du média SAMI](sami-media-source.md)
</dt> </dl>

 

 




