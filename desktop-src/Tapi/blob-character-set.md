---
description: L' \_ énumération du jeu de caractères BLOB \_ indique le jeu de caractères utilisé par l’objet blob de conférence actuel.
ms.assetid: 79131b84-19b5-492b-a44e-9d47c365b298
title: Énumération BLOB_CHARACTER_SET (sdpblb. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 66b180a8574f1643a5fc1be134be99c951faaf1d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106533101"
---
# <a name="blob_character_set-enumeration"></a>\_Énumération du jeu de caractères BLOB \_

\[ Les interfaces et les contrôles de conférence de téléphonie IP Rendezvous ne peuvent pas être utilisés dans Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation. L’API cliente RTC offre des fonctionnalités similaires.\]

L’énumération du **\_ \_ jeu de caractères BLOB** indique le jeu de caractères utilisé par l’objet blob de conférence actuel.

## <a name="syntax"></a>Syntaxe


```C++
} BLOB_CHARACTER_SET;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="BCS_ASCII"></span><span id="bcs_ascii"></span>**\_ASCII BCS**
</dt> <dd>

Format ASCII standard.

</dd> <dt>

<span id="BCS_UTF7"></span><span id="bcs_utf7"></span>**UTF7 pour BCS \_**
</dt> <dd>

Format de transformation 7 bits Unicode. Pour plus d’informations sur ce format, lancez une recherche sur Internet pour la RFC 1642.

</dd> <dt>

<span id="BCS_UTF8"></span><span id="bcs_utf8"></span>**SBC \_ UTF8**
</dt> <dd>

Format de transformation UCS 8. Pour plus d’informations sur ce format, lancez une recherche sur Internet ISO (le Organisation internationale de normalisation) et IEC (le Commission Électrotechnique Internationale) document ISO/IEC JTC1/SC2/WG2 N 1036, datée du 1er août 1994, par WG2 Project Editor.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------|-------------------------------------------------------------------------------------|
| Version TAPI<br/> | Nécessite TAPI 3,0 ou une version ultérieure<br/>                                               |
| En-tête<br/>       | <dl> <dt>Sdpblb. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**ITDirectoryObjectConference**](/windows/desktop/api/Rend/nn-rend-itdirectoryobjectconference)
</dt> <dt>

[**Obtient \_ CharacterSet**](itconferenceblob-get-characterset.md)
</dt> <dt>

[**Rein**](itconferenceblob-init.md)
</dt> <dt>

[**SetConferenceBlob**](itconferenceblob-setconferenceblob.md)
</dt> </dl>

 

 




