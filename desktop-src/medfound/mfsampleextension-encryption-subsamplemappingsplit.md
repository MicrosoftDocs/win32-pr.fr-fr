---
description: Définit le mappage de sous-échantillon pour l’exemple indiquant les octets clairs et chiffrés dans les exemples de données.
ms.assetid: E672F53D-2083-430B-90D2-A1DA482EF9E1
title: Attribut MFSampleExtension_Encryption_SubSampleMappingSplit (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 19f10f845b337ab92774f36b46940fe9d5203ca3a672f573e33fbcea26e96e16
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118240792"
---
# <a name="mfsampleextension_encryption_subsamplemappingsplit-attribute"></a>\_Attribut SubSampleMappingSplit de chiffrement MFSampleExtension \_

Définit le mappage de sous-échantillon pour l’exemple indiquant les octets clairs et chiffrés dans les exemples de données.

## <a name="data-type"></a>Type de données

**OBJET BLOB**

## <a name="remarks"></a>Notes

L' **objet BLOB** doit contenir un tableau de plages d’octets en tant que DWORDS, où tous les deux DWORD effectuent un ensemble. Le premier DWORD de chaque jeu est le nombre d’octets clairs et le deuxième DWORD de l’ensemble est le nombre d’octets chiffrés. Notez qu’une paire de 0 n’est pas un ensemble valide (l’une des valeurs peut être 0, mais pas les deux). Le tableau de plages d’octets indique les plages à déchiffrer, y compris la possibilité de déchiffrer la totalité de l’échantillon. Il est recommandé de ne pas définir ce paramètre sur les exemples clairs, bien qu’il soit possible d’obtenir le même résultat en le définissant avec les valeurs appropriées.

## <a name="examples"></a>Exemples

L’exemple suivant montre comment définir le \_ chiffrement de MFSampleExtension \_ SubSampleMappingSplit.


```C++
// m_spSample is a IMFSample
// pdwSubSampleMap is a DWORD*
// dwSubSampleMapSize is a DWORD

m_spSample->SetBlob( MFSampleExtension_Encryption_SubSampleMappingSplit,
                    (BYTE*)pdwSubSampleMap, 
                    dwSubSampleMapSize * sizeof(DWORD) );
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | \[applications Windows 8.1 desktop apps \| UWP\]<br/>                                |
| Serveur minimal pris en charge<br/> | Windows Server 2012 Applications de \[ Bureau R2 \| applications UWP\]<br/>                     |
| En-tête<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Liste alphabétique des attributs Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)
</dt> <dt>

[MFSampleExtension de \_ contenu \_ KeyId](mfsampleextension-content-keyid.md)
</dt> </dl>

 

 




