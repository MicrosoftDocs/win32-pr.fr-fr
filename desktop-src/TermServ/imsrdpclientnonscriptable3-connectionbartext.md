---
title: IMsRdpClientNonScriptable3 propriété ConnectionBarText
description: Définit ou récupère le texte pour mettre à jour la barre de connexion.
ms.assetid: 9671118d-ee7c-4077-be81-57655aff5e35
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété ConnectionBarText
- Services Bureau à distance de la propriété ConnectionBarText, interface IMsRdpClientNonScriptable3
- Services Bureau à distance de l’interface IMsRdpClientNonScriptable3, propriété ConnectionBarText
- Services Bureau à distance de la propriété ConnectionBarText, interface IMsRdpClientNonScriptable4
- Services Bureau à distance de l’interface IMsRdpClientNonScriptable4, propriété ConnectionBarText
- Services Bureau à distance de la propriété ConnectionBarText, interface IMsRdpClientNonScriptable5
- Services Bureau à distance de l’interface IMsRdpClientNonScriptable5, propriété ConnectionBarText
- Services Bureau à distance de la propriété ConnectionBarText, objet MsRdpClient5
- Services Bureau à distance objet MsRdpClient5, propriété ConnectionBarText
- Services Bureau à distance de la propriété ConnectionBarText, objet MsRdpClient6
- Services Bureau à distance objet MsRdpClient6, propriété ConnectionBarText
- Services Bureau à distance de la propriété ConnectionBarText, objet MsRdpClient7
- Services Bureau à distance objet MsRdpClient7, propriété ConnectionBarText
- Services Bureau à distance de la propriété ConnectionBarText, objet MsRdpClient8
- Services Bureau à distance objet MsRdpClient8, propriété ConnectionBarText
- Services Bureau à distance de la propriété ConnectionBarText, objet MsRdpClient9
- Services Bureau à distance objet MsRdpClient9, propriété ConnectionBarText
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable3.ConnectionBarText
- IMsRdpClientNonScriptable3.get_ConnectionBarText
- IMsRdpClientNonScriptable3.put_ConnectionBarText
- IMsRdpClientNonScriptable4.ConnectionBarText
- IMsRdpClientNonScriptable4.get_ConnectionBarText
- IMsRdpClientNonScriptable4.put_ConnectionBarText
- IMsRdpClientNonScriptable5.ConnectionBarText
- IMsRdpClientNonScriptable5.get_ConnectionBarText
- IMsRdpClientNonScriptable5.put_ConnectionBarText
- MsRdpClient5.ConnectionBarText
- MsRdpClient6.ConnectionBarText
- MsRdpClient7.ConnectionBarText
- MsRdpClient8.ConnectionBarText
- MsRdpClient9.ConnectionBarText
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 76819dd28ffd8b2ee5e2dfb30017e341dd49db5b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743293"
---
# <a name="imsrdpclientnonscriptable3connectionbartext-property"></a>IMsRdpClientNonScriptable3 :: ConnectionBarText, propriété

Définit ou récupère le texte pour mettre à jour la barre de connexion.

Cette propriété est en lecture/écriture.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT put_ConnectionBarText(
  [in]  BSTR newVal
);

HRESULT get_ConnectionBarText(
  [out] BSTR *pConnectionBarText
);
```



## <a name="property-value"></a>Valeur de la propriété

Définit la chaîne de texte à afficher dans la barre de connexion.

## <a name="remarks"></a>Notes

Vous devez appeler la méthode **IMsRdpClientNonScriptable3 ::p ut \_ ConnectionBarText** avant d’appeler la méthode [**IMsTscSecuredSettings ::P ut \_ fullscreen**](imstscsecuredsettings-fullscreen.md) ou [**IMsRdpClient ::p ut \_ fullscreen**](imsrdpclient-fullscreen.md) .

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

 

 





