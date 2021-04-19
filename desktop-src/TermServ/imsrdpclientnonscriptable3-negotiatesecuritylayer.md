---
title: IMsRdpClientNonScriptable3 propriété NegotiateSecurityLayer
description: Spécifie ou récupère si la couche de sécurité de négociation est activée pour la connexion.
ms.assetid: 7fc9e3c7-0723-48c4-8d29-5f68a24a522c
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété NegotiateSecurityLayer
- Services Bureau à distance de la propriété NegotiateSecurityLayer, interface IMsRdpClientNonScriptable3
- Services Bureau à distance de l’interface IMsRdpClientNonScriptable3, propriété NegotiateSecurityLayer
- Services Bureau à distance de la propriété NegotiateSecurityLayer, interface IMsRdpClientNonScriptable4
- Services Bureau à distance de l’interface IMsRdpClientNonScriptable4, propriété NegotiateSecurityLayer
- Services Bureau à distance de la propriété NegotiateSecurityLayer, interface IMsRdpClientNonScriptable5
- Services Bureau à distance de l’interface IMsRdpClientNonScriptable5, propriété NegotiateSecurityLayer
- Services Bureau à distance de la propriété NegotiateSecurityLayer, objet MsRdpClient5
- Services Bureau à distance objet MsRdpClient5, propriété NegotiateSecurityLayer
- Services Bureau à distance de la propriété NegotiateSecurityLayer, objet MsRdpClient6
- Services Bureau à distance objet MsRdpClient6, propriété NegotiateSecurityLayer
- Services Bureau à distance de la propriété NegotiateSecurityLayer, objet MsRdpClient7
- Services Bureau à distance objet MsRdpClient7, propriété NegotiateSecurityLayer
- Services Bureau à distance de la propriété NegotiateSecurityLayer, objet MsRdpClient8
- Services Bureau à distance objet MsRdpClient8, propriété NegotiateSecurityLayer
- Services Bureau à distance de la propriété NegotiateSecurityLayer, objet MsRdpClient9
- Services Bureau à distance objet MsRdpClient9, propriété NegotiateSecurityLayer
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable3.NegotiateSecurityLayer
- IMsRdpClientNonScriptable3.get_NegotiateSecurityLayer
- IMsRdpClientNonScriptable3.put_NegotiateSecurityLayer
- IMsRdpClientNonScriptable4.NegotiateSecurityLayer
- IMsRdpClientNonScriptable4.get_NegotiateSecurityLayer
- IMsRdpClientNonScriptable4.put_NegotiateSecurityLayer
- IMsRdpClientNonScriptable5.NegotiateSecurityLayer
- IMsRdpClientNonScriptable5.get_NegotiateSecurityLayer
- IMsRdpClientNonScriptable5.put_NegotiateSecurityLayer
- MsRdpClient5.NegotiateSecurityLayer
- MsRdpClient6.NegotiateSecurityLayer
- MsRdpClient7.NegotiateSecurityLayer
- MsRdpClient8.NegotiateSecurityLayer
- MsRdpClient9.NegotiateSecurityLayer
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e64533615c780cd6e3703be85363684e537b784a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106540776"
---
# <a name="imsrdpclientnonscriptable3negotiatesecuritylayer-property"></a>IMsRdpClientNonScriptable3 :: NegotiateSecurityLayer, propriété

Spécifie ou récupère si la couche de sécurité de négociation est activée pour la connexion.

Cette propriété est en lecture/écriture.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT put_NegotiateSecurityLayer(
  [in]  VARIANT_BOOL fNegotiate
);

HRESULT get_NegotiateSecurityLayer(
  [out] VARIANT_BOOL *pfNegotiate
);
```



## <a name="property-value"></a>Valeur de la propriété

Spécifie s’il faut activer la négociation de la couche de sécurité.

## <a name="remarks"></a>Notes

Si cette propriété est définie sur **\_ false** et que authentification au niveau du réseau (NLA) est activé sur le système d’exploitation client, le client ne négociera pas la couche de sécurité et utilisera NLA pour sécuriser la connexion RDP. Si cette propriété a la valeur **Variant \_ true**, le client négocie entre NLA et la sécurité RDP de base.

> [!Note]  
> La désactivation de la négociation de la couche de sécurité est possible uniquement lors de la connexion à un serveur hôte de session Bureau à distance (hôte de session Bureau à distance) exécutant Windows Vista ou des systèmes d’exploitation ultérieurs. Si cette propriété est activée et que le client tente de se connecter à un serveur hôte de session Bureau à distance exécutant un système d’exploitation antérieur, la connexion échoue.

 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                                      |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                                |
| Bibliothèque de types<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>        |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>        |
| IID<br/>                      | IID \_ IMsRdpClientNonScriptable3 est défini en tant que b3378d90-0728-45c7-8ed7-b6159fb92219<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IMsRdpClientNonScriptable4**](imsrdpclientnonscriptable4.md)
</dt> <dt>

[**IMsRdpClientNonScriptable5**](imsrdpclientnonscriptable5.md)
</dt> <dt>

[**IMsRdpClientNonScriptable3**](imsrdpclientnonscriptable3.md)
</dt> </dl>

 

 





