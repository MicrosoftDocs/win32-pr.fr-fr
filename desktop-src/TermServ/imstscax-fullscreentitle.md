---
title: IMsTscAx propriété FullScreenTitle
description: Spécifie le titre de la fenêtre qui s’affiche lorsque le contrôle est en mode plein écran.
ms.assetid: 441aea43-2d1c-44b7-a74f-e375e711fb4f
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété FullScreenTitle
- Services Bureau à distance de la propriété FullScreenTitle, interface IMsTscAx
- Services Bureau à distance de l’interface IMsTscAx, propriété FullScreenTitle
- Services Bureau à distance de la propriété FullScreenTitle, interface IMsRdpClient
- Services Bureau à distance de l’interface IMsRdpClient, propriété FullScreenTitle
- Services Bureau à distance de la propriété FullScreenTitle, interface IMsRdpClient2
- Services Bureau à distance de l’interface IMsRdpClient2, propriété FullScreenTitle
- Services Bureau à distance de la propriété FullScreenTitle, interface IMsRdpClient3
- Services Bureau à distance de l’interface IMsRdpClient3, propriété FullScreenTitle
- Services Bureau à distance de la propriété FullScreenTitle, interface IMsRdpClient4
- Services Bureau à distance de l’interface IMsRdpClient4, propriété FullScreenTitle
- Services Bureau à distance de la propriété FullScreenTitle, interface IMsRdpClient5
- Services Bureau à distance de l’interface IMsRdpClient5, propriété FullScreenTitle
- Services Bureau à distance de la propriété FullScreenTitle, interface IMsRdpClient6
- Services Bureau à distance de l’interface IMsRdpClient6, propriété FullScreenTitle
- Services Bureau à distance de la propriété FullScreenTitle, interface IMsRdpClient7
- Services Bureau à distance de l’interface IMsRdpClient7, propriété FullScreenTitle
- Services Bureau à distance de la propriété FullScreenTitle, interface IMsRdpClient8
- Services Bureau à distance de l’interface IMsRdpClient8, propriété FullScreenTitle
- Services Bureau à distance de la propriété FullScreenTitle, interface IMsRdpClient9
- Services Bureau à distance de l’interface IMsRdpClient9, propriété FullScreenTitle
topic_type:
- apiref
api_name:
- IMsTscAx.FullScreenTitle
- IMsTscAx.put_FullScreenTitle
- IMsRdpClient.FullScreenTitle
- IMsRdpClient.put_FullScreenTitle
- IMsRdpClient2.FullScreenTitle
- IMsRdpClient2.put_FullScreenTitle
- IMsRdpClient3.FullScreenTitle
- IMsRdpClient3.put_FullScreenTitle
- IMsRdpClient4.FullScreenTitle
- IMsRdpClient4.put_FullScreenTitle
- IMsRdpClient5.FullScreenTitle
- IMsRdpClient5.put_FullScreenTitle
- IMsRdpClient6.FullScreenTitle
- IMsRdpClient6.put_FullScreenTitle
- IMsRdpClient7.FullScreenTitle
- IMsRdpClient7.put_FullScreenTitle
- IMsRdpClient8.FullScreenTitle
- IMsRdpClient8.put_FullScreenTitle
- IMsRdpClient9.FullScreenTitle
- IMsRdpClient9.put_FullScreenTitle
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1384d1582f4f0089df55030c22471438575bd072
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104326"
---
# <a name="imstscaxfullscreentitle-property"></a>IMsTscAx :: FullScreenTitle, propriété

Spécifie le titre de la fenêtre qui s’affiche lorsque le contrôle est en mode plein écran.

Cette propriété est en écriture seule.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT put_FullScreenTitle(
  [in] BSTR fullScreenTitle
);
```



## <a name="property-value"></a>Valeur de la propriété

Titre de la fenêtre. La longueur maximale de cette chaîne est le \_ chemin d’accès maximal-1 caractères.

## <a name="error-codes"></a>Codes d’erreur

Retourne **S \_ OK** en cas de réussite.

## <a name="remarks"></a>Notes

Cette propriété est utilisée pour définir le titre de la fenêtre du contrôle lorsque la connexion est ouverte en mode plein écran. N’utilisez pas cette propriété pour le mode plein écran géré par le conteneur. Lorsque la méthode [**IMsTscAdvancedSettings ::p ut \_ ContainerHandledFullScreen**](imstscadvancedsettings-containerhandledfullscreen.md) est appelée, la fenêtre de conteneur affiche le titre de la fenêtre.

Pour plus d’informations sur la Connexion Bureau à distance par le Web, consultez [Requirements for connexion Bureau à distance par le Web](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                               |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                         |
| Bibliothèque de types<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IID \_ IMsTscAx est défini en tant que 8C11EFAE-92C3-11D1-BC1E-00C04FA31489<br/>            |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IMsRdpClient**](imsrdpclient-interface.md)
</dt> <dt>

[**IMsRdpClient2**](imsrdpclient2.md)
</dt> <dt>

[**IMsRdpClient3**](imsrdpclient3.md)
</dt> <dt>

[**IMsRdpClient4**](imsrdpclient4.md)
</dt> <dt>

[**IMsRdpClient5**](imsrdpclient5.md)
</dt> <dt>

[**IMsRdpClient6**](imsrdpclient6.md)
</dt> <dt>

[**IMsRdpClient7**](imsrdpclient7.md)
</dt> <dt>

[**IMsRdpClient8**](imsrdpclient8.md)
</dt> <dt>

[**IMsRdpClient9**](imsrdpclient9.md)
</dt> <dt>

[**IMsTscAx**](imstscax-interface.md)
</dt> </dl>

 

 





