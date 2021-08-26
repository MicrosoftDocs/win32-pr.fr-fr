---
title: IMsTscNonScriptable propriété ClearTextPassword
description: définit le Bureau à distance ActiveX mot de passe de contrôle au format texte en clair.
ms.assetid: 93d35b10-5c92-4ab7-a32a-328ba6fcf16b
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété ClearTextPassword
- Services Bureau à distance de la propriété ClearTextPassword, interface IMsTscNonScriptable
- Services Bureau à distance de l’interface IMsTscNonScriptable, propriété ClearTextPassword
- Services Bureau à distance de la propriété ClearTextPassword, interface IMsRdpClientNonScriptable
- Services Bureau à distance de l’interface IMsRdpClientNonScriptable, propriété ClearTextPassword
- Services Bureau à distance de la propriété ClearTextPassword, interface IMsRdpClientNonScriptable2
- Services Bureau à distance de l’interface IMsRdpClientNonScriptable2, propriété ClearTextPassword
- Services Bureau à distance de la propriété ClearTextPassword, interface IMsRdpClientNonScriptable3
- Services Bureau à distance de l’interface IMsRdpClientNonScriptable3, propriété ClearTextPassword
- Services Bureau à distance de la propriété ClearTextPassword, interface IMsRdpClientNonScriptable4
- Services Bureau à distance de l’interface IMsRdpClientNonScriptable4, propriété ClearTextPassword
- Services Bureau à distance de la propriété ClearTextPassword, interface IMsRdpClientNonScriptable5
- Services Bureau à distance de l’interface IMsRdpClientNonScriptable5, propriété ClearTextPassword
- Services Bureau à distance de la propriété ClearTextPassword, objet MsRdpClient6
- Services Bureau à distance objet MsRdpClient6, propriété ClearTextPassword
- Services Bureau à distance de la propriété ClearTextPassword, objet MsRdpClient7
- Services Bureau à distance objet MsRdpClient7, propriété ClearTextPassword
- Services Bureau à distance de la propriété ClearTextPassword, objet MsRdpClient8
- Services Bureau à distance objet MsRdpClient8, propriété ClearTextPassword
- Services Bureau à distance de la propriété ClearTextPassword, objet MsRdpClient9
- Services Bureau à distance objet MsRdpClient9, propriété ClearTextPassword
topic_type:
- apiref
api_name:
- IMsTscNonScriptable.ClearTextPassword
- IMsTscNonScriptable.put_ClearTextPassword
- IMsRdpClientNonScriptable.ClearTextPassword
- IMsRdpClientNonScriptable.put_ClearTextPassword
- IMsRdpClientNonScriptable2.ClearTextPassword
- IMsRdpClientNonScriptable2.put_ClearTextPassword
- IMsRdpClientNonScriptable3.ClearTextPassword
- IMsRdpClientNonScriptable3.put_ClearTextPassword
- IMsRdpClientNonScriptable4.ClearTextPassword
- IMsRdpClientNonScriptable4.put_ClearTextPassword
- IMsRdpClientNonScriptable5.ClearTextPassword
- IMsRdpClientNonScriptable5.put_ClearTextPassword
- MsRdpClient6.ClearTextPassword
- MsRdpClient7.ClearTextPassword
- MsRdpClient8.ClearTextPassword
- MsRdpClient9.ClearTextPassword
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0519e7379eab529cc5275c85a11116764417d524a03dff2e1eab74a914b6560b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120125049"
---
# <a name="imstscnonscriptablecleartextpassword-property"></a>IMsTscNonScriptable :: ClearTextPassword, propriété

définit le Bureau à distance ActiveX mot de passe de contrôle au format texte en clair.

Cette propriété est en écriture seule.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT put_ClearTextPassword(
  [in] BSTR newClearTextPass
);
```



## <a name="property-value"></a>Valeur de la propriété

Mot de passe à utiliser pour la connexion, spécifié au format texte en clair.

## <a name="error-codes"></a>Codes d’erreur

Retourne **S \_ OK** en cas de réussite.

## <a name="remarks"></a>Remarques

Le mot de passe est transmis au serveur dans le canal de communications RDP chiffré en toute sécurité. Une fois qu’un mot de passe en texte clair est défini, il ne peut pas être récupéré au format texte brut.

la propriété **ClearTextPassword** ne peut être définie que lorsque le Bureau à distance ActiveX contrôle n’est pas dans l’état connecté. La définition de cette propriété échoue si le contrôle est connecté. Pour vérifier l’état connecté, récupérez la propriété [**IMsTscAx :: Connected**](imstscax-connected.md) .

Vous pouvez également appeler cette méthode pour définir un mot de passe en texte clair avant de le convertir en un mot de passe encodé portable ou en un mot de passe encodé binaire (non transférable). Notez cependant que les mots de passe encodés ne doivent pas être considérés comme étant chiffrés de manière sécurisée.

Si vous appelez pour la première fois cette méthode pour définir un mot de passe au format texte brut, vous pouvez convertir le mot de passe au format encodé.

**Pour convertir un mot de passe en texte clair au format encodé**

1.  Définissez le mot de passe au format texte en clair dans la propriété **ClearTextPassword** .
2.  Pour récupérer le mot de passe dans un format encodé binaire (à l’importable), récupérez la propriété [**BinaryPassword**](imstscnonscriptable-binarypassword.md) et les propriétés [**BinarySalt**](imstscnonscriptable-binarysalt.md) . La partie de mot de passe encodée et la partie Salt sont requises pour définir un mot de passe au format encodé binaire.
3.  Pour récupérer le mot de passe dans un format encodé portable, récupérez la méthode [**PortablePassword**](imstscnonscriptable-portablepassword.md) et les propriétés [**PortableSalt**](imstscnonscriptable-portablesalt.md) . Les deux parties sont requises pour définir un mot de passe dans un format encodé portable.

Après avoir suivi les trois étapes précédentes, vous pouvez définir le mot de passe au format encodé en définissant les propriétés [**BinaryPassword**](imstscnonscriptable-binarypassword.md) et [**BinarySalt**](imstscnonscriptable-binarysalt.md) , ou les propriétés [**PortablePassword**](imstscnonscriptable-portablepassword.md) et [**PortableSalt**](imstscnonscriptable-portablesalt.md) . Les deux parties sont requises.

Pour activer l’ouverture de session automatique, vous devez également définir les propriétés de [**nom d’utilisateur**](imstscax-username.md) et de [**domaine**](imstscax-domain.md) . si le mot de passe ne parvient pas à authentifier l’utilisateur, la boîte de dialogue d’ouverture de session Windows s’affiche sur le serveur pour inviter l’utilisateur à entrer le mot de passe.

Pour plus d’informations sur la Connexion Bureau à distance par le Web, consultez [Requirements for connexion Bureau à distance par le Web](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                               |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                         |
| Bibliothèque de types<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IID \_ IMsTscNonScriptable est défini en tant que c1e6743a-41c1-4a74-832a-0dd06c1c7a0e<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IMsRdpClientNonScriptable**](imsrdpclientnonscriptable-interface.md)
</dt> <dt>

[**IMsRdpClientNonScriptable2**](imsrdpclientnonscriptable2.md)
</dt> <dt>

[**IMsRdpClientNonScriptable3**](imsrdpclientnonscriptable3.md)
</dt> <dt>

[**IMsRdpClientNonScriptable4**](imsrdpclientnonscriptable4.md)
</dt> <dt>

[**IMsRdpClientNonScriptable5**](imsrdpclientnonscriptable5.md)
</dt> <dt>

[**IMsTscNonScriptable**](imstscnonscriptable-interface.md)
</dt> </dl>

 

 





