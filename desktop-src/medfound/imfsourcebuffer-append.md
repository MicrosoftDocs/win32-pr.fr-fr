---
description: Ajoute le segment de média spécifié à IMFSourceBuffer.
ms.assetid: 824fa23d-57d9-411a-af8a-fb65dca124b2
title: 'IMFSourceBuffer :: Append, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMFSourceBuffer.Append
api_type:
- COM
api_location:
- mfmediaengine.h
ms.openlocfilehash: 00c9b6a0af2e48482311a8a0e1bc39dc4ce951aa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201728"
---
# <a name="imfsourcebufferappend-method"></a>IMFSourceBuffer :: Append, méthode

Ajoute le segment de média spécifié à [**IMFSourceBuffer**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfsourcebuffer).

## <a name="syntax"></a>Syntaxe


```C++
HRESULT Append(
  [in] const BYTE  *pData,
  [in]       DWORD len
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pData* \[ dans\]
</dt> <dd>

Données multimédia à ajouter.

</dd> <dt>

*Len* \[ dans\]
</dt> <dd>

Longueur des données de média stockées dans *pData*.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si cette méthode est réussie, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8.1 les \[ applications de bureau uniquement\]<br/>                                                 |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2012 R2 \[ uniquement\]<br/>                                      |
| MIDL<br/>                      | <dl> <dt>Mfmediaengine. idl</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IMFSourceBuffer**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfsourcebuffer)
</dt> </dl>

 

 




