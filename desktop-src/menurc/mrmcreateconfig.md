---
title: MrmCreateConfig, fonction (MrmResourceIndexer. h)
description: Crée un nouveau fichier de configuration PRI initialisé définissant les valeurs par défaut du qualificateur que vous spécifiez. Pour plus d’informations et pour obtenir des procédures pas à pas sur l’utilisation de ces API, consultez API PRI (package Resource Indexing) et systèmes de génération personnalisés.
ms.assetid: F8FB4E9C-1C04-460A-BFA1-FB663653DA3C
keywords:
- Menus de fonction MrmCreateConfig et autres ressources
topic_type:
- apiref
api_name:
- MrmCreateConfig
api_location:
- Mrmsupport.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3adb270d9bbd9194822181314a697fa1d267a127
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127235697"
---
# <a name="mrmcreateconfig-function"></a>MrmCreateConfig fonction)

\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation. Microsoft exclut toute garantie, expresse ou implicite, concernant les informations fournies ici.\]

Crée un nouveau fichier de configuration PRI initialisé définissant les valeurs par défaut du qualificateur que vous spécifiez. Pour plus d’informations et pour obtenir des procédures pas à pas sur l’utilisation de ces API, consultez [API PRI (package Resource Indexing) et systèmes de génération personnalisés](/windows/uwp/app-resources/pri-apis-custom-build-systems).

## <a name="syntax"></a>Syntaxe


```C++
HRESULT HRESULT MrmCreateConfig(
  _In_     MrmPlatformVersion platformVersion,
  _In_opt_ PCWSTR             defaultQualifiers,
  _In_     PCWSTR             outputXmlFile
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*platformVersion* \[ dans\]
</dt> <dd>

Type : **[ **MrmPlatformVersion**](mrmplatformversion.md)**

Version de la plateforme (*targetOsVersion*) à utiliser pour le fichier de configuration généré.

</dd> <dt>

*defaultQualifiers* \[ dans, facultatif\]
</dt> <dd>

Type : **PCWSTR**

Liste des qualificateurs de ressources par défaut. Par exemple, L « language-en-US \_ Scale-100 \_ Contrast-standard »

</dd> <dt>

*outputXmlFile* \[ dans\]
</dt> <dd>

Type : **PCWSTR**

Chemin d’accès du fichier de configuration à créer.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Type : **HRESULT**

\_OK si la fonction a réussi, sinon une autre valeur. Utilisez les macros SUCCEEDED () ou FAILed () (définies dans Winerror. h) pour déterminer la réussite ou l’échec.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 10, les applications de bureau version 1803 \[ uniquement\]<br/>                                       |
| Serveur minimal pris en charge<br/> | Windows \[Applications de bureau serveur uniquement\]<br/>                                                 |
| En-tête<br/>                   | <dl> <dt>MrmResourceIndexer. h</dt> </dl> |
| Bibliothèque<br/>                  | <dl> <dt>Mrmsupport. lib</dt> </dl>       |
| DLL<br/>                      | <dl> <dt>Mrmsupport.dll</dt> </dl>       |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[API d’indexation de ressources de package (IRP) et systèmes de génération personnalisés](/windows/uwp/app-resources/pri-apis-custom-build-systems)
</dt> </dl>

 

