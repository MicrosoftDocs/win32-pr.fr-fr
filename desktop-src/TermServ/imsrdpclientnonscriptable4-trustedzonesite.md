---
title: IMsRdpClientNonScriptable4 propriété TrustedZoneSite
description: Spécifie si le site Web à partir duquel l’utilisateur a lancé la connexion se trouve dans la liste des sites de confiance de l’ordinateur client de l’utilisateur.
ms.assetid: cb7efacc-b13b-494c-ab02-35c4f914744c
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété TrustedZoneSite
- Services Bureau à distance de la propriété TrustedZoneSite, interface IMsRdpClientNonScriptable4
- Services Bureau à distance de l’interface IMsRdpClientNonScriptable4, propriété TrustedZoneSite
- Services Bureau à distance de la propriété TrustedZoneSite, interface IMsRdpClientNonScriptable5
- Services Bureau à distance de l’interface IMsRdpClientNonScriptable5, propriété TrustedZoneSite
- Services Bureau à distance de la propriété TrustedZoneSite, objet MsRdpClient6
- Services Bureau à distance objet MsRdpClient6, propriété TrustedZoneSite
- Services Bureau à distance de la propriété TrustedZoneSite, objet MsRdpClient7
- Services Bureau à distance objet MsRdpClient7, propriété TrustedZoneSite
- Services Bureau à distance de la propriété TrustedZoneSite, objet MsRdpClient8
- Services Bureau à distance objet MsRdpClient8, propriété TrustedZoneSite
- Services Bureau à distance de la propriété TrustedZoneSite, objet MsRdpClient9
- Services Bureau à distance objet MsRdpClient9, propriété TrustedZoneSite
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable4.TrustedZoneSite
- IMsRdpClientNonScriptable4.get_TrustedZoneSite
- IMsRdpClientNonScriptable4.put_TrustedZoneSite
- IMsRdpClientNonScriptable5.TrustedZoneSite
- IMsRdpClientNonScriptable5.get_TrustedZoneSite
- IMsRdpClientNonScriptable5.put_TrustedZoneSite
- MsRdpClient6.TrustedZoneSite
- MsRdpClient7.TrustedZoneSite
- MsRdpClient8.TrustedZoneSite
- MsRdpClient9.TrustedZoneSite
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d791b5eff3346f61f999ea1f4f78bc41a5acea0e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127008608"
---
# <a name="imsrdpclientnonscriptable4trustedzonesite-property"></a>IMsRdpClientNonScriptable4 :: TrustedZoneSite, propriété

Spécifie si le site Web à partir duquel l’utilisateur a lancé la connexion se trouve dans la liste des sites de confiance de l’ordinateur client de l’utilisateur.

Cette propriété est en lecture/écriture.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_TrustedZoneSite(
  [in]  VARIANT_BOOL fIsTrustedZone
);

HRESULT get_TrustedZoneSite(
  [out] VARIANT_BOOL *pfIsTrustedZone
);
```



## <a name="property-value"></a>Valeur de la propriété

Définit la propriété TrustedZoneSite. Cette méthode n’a aucun effet sur le fait que le site Web à partir duquel l’utilisateur a lancé la connexion se trouve dans la liste des sites de confiance de l’ordinateur client.

## <a name="error-codes"></a>Codes d’erreur

Retourne **S \_ OK** en cas de réussite.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                                 |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                           |
| Bibliothèque de types<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>   |
| IID<br/>                      | IMsRdpClientNonScriptable4 est défini en tant que f50fa8aa-1c7d-4f59-B15C-a90cacae1fcb<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IMsRdpClientNonScriptable5**](imsrdpclientnonscriptable5.md)
</dt> <dt>

[**IMsRdpClientNonScriptable4**](imsrdpclientnonscriptable4.md)
</dt> </dl>

 

 





