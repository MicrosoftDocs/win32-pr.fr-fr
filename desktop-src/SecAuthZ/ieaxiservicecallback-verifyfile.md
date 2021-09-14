---
description: effectue des vérifications de sécurité sur l’objet ActiveX spécifié et retourne l’emplacement où le fichier .cab correspondant a été téléchargé.
ms.assetid: ba8e4f9b-1569-43f9-b27c-a987044fff41
title: 'IeAxiServiceCallback :: VerifyFile, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IeAxiServiceCallback.VerifyFile
api_type:
- COM
api_location: ''
ms.openlocfilehash: 6d590f5e0e7ecd881a51844737f8efddf34d6727
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127096070"
---
# <a name="ieaxiservicecallbackverifyfile-method"></a>IeAxiServiceCallback :: VerifyFile, méthode

la méthode **VerifyFile** effectue des vérifications de sécurité sur l’objet ActiveX spécifié et retourne l’emplacement où le fichier .cab correspondant a été téléchargé.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT VerifyFile(
  [in]  BSTR bstrFileUrl,
  [out] BSTR *bstrApprovedFileName
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*bstrFileUrl* \[ dans\]
</dt> <dd>

URL de l’objet ActiveX à vérifier.

</dd> <dt>

*bstrApprovedFileName* \[ à\]
</dt> <dd>

nom du fichier dans lequel le .cab fichier associé à l’objet ActiveX a été téléchargé.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Si la méthode est réussie, la méthode retourne S \_ OK.

Si la méthode échoue, elle retourne une valeur **HRESULT** qui indique l’erreur. Pour obtenir la liste des codes d’erreur courants, consultez [valeurs HRESULT communes](/windows/desktop/SecCrypto/common-hresult-values).

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows vista Business, Windows vista Enterprise, Windows les applications de bureau vista Ultimate \[ uniquement\]<br/> |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                                 |
| IID<br/>                      | IID \_ IeAxiServiceCallback est défini en tant que 1823E7BA-EC36-447A-9B2E-B4912E15AFE7<br/>                   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IeAxiServiceCallback**](ieaxiservicecallback.md)
</dt> </dl>

 

