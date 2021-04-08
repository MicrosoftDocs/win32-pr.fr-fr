---
title: IMsRdpClientNonScriptable4 propriété PublisherCertificateChain
description: Contrôle la chaîne du certificat de l’éditeur. La chaîne est stockée dans un variant de type VT \_ ByRef qui contient un pointeur vers une \_ structure de contexte de chaîne du certificat \_ . Pour plus d’informations sur les structures de type de données VT \_ , consultez variant et VARIANTARG.
ms.assetid: 27ab0aff-1aef-4701-abe0-849bf32c9773
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété PublisherCertificateChain
- Services Bureau à distance de la propriété PublisherCertificateChain, interface IMsRdpClientNonScriptable4
- Services Bureau à distance de l’interface IMsRdpClientNonScriptable4, propriété PublisherCertificateChain
- Services Bureau à distance de la propriété PublisherCertificateChain, interface IMsRdpClientNonScriptable5
- Services Bureau à distance de l’interface IMsRdpClientNonScriptable5, propriété PublisherCertificateChain
- Services Bureau à distance de la propriété PublisherCertificateChain, objet MsRdpClient6
- Services Bureau à distance objet MsRdpClient6, propriété PublisherCertificateChain
- Services Bureau à distance de la propriété PublisherCertificateChain, objet MsRdpClient7
- Services Bureau à distance objet MsRdpClient7, propriété PublisherCertificateChain
- Services Bureau à distance de la propriété PublisherCertificateChain, objet MsRdpClient8
- Services Bureau à distance objet MsRdpClient8, propriété PublisherCertificateChain
- Services Bureau à distance de la propriété PublisherCertificateChain, objet MsRdpClient9
- Services Bureau à distance objet MsRdpClient9, propriété PublisherCertificateChain
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable4.PublisherCertificateChain
- IMsRdpClientNonScriptable4.get_PublisherCertificateChain
- IMsRdpClientNonScriptable4.put_PublisherCertificateChain
- IMsRdpClientNonScriptable5.PublisherCertificateChain
- IMsRdpClientNonScriptable5.get_PublisherCertificateChain
- IMsRdpClientNonScriptable5.put_PublisherCertificateChain
- MsRdpClient6.PublisherCertificateChain
- MsRdpClient7.PublisherCertificateChain
- MsRdpClient8.PublisherCertificateChain
- MsRdpClient9.PublisherCertificateChain
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7552483c2fc651ace1a9401e0555f90fb2584423
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843853"
---
# <a name="imsrdpclientnonscriptable4publishercertificatechain-property"></a>IMsRdpClientNonScriptable4 ::P propriété ublisherCertificateChain

Contrôle la chaîne du certificat de l’éditeur. La chaîne est stockée dans un variant de type **VT \_ ByRef** qui contient un pointeur vers une structure de [**\_ \_ contexte de chaîne du certificat**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_chain_context) . Pour plus d’informations sur les structures de type de données **VT \_** , consultez [Variant et VARIANTARG](/windows/win32/api/oaidl/ns-oaidl-variant).

Cette propriété est en lecture/écriture.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT put_PublisherCertificateChain(
  [in]  VARIANT *pVarCert
);

HRESULT get_PublisherCertificateChain(
  [out] VARIANT *pVarCert
);
```



## <a name="property-value"></a>Valeur de la propriété

Définit la chaîne du certificat de l’éditeur. La chaîne est stockée dans un variant de type **VT \_ ByRef** qui contient un pointeur vers une structure de [**\_ \_ contexte de chaîne du certificat**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_chain_context) .

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

 

