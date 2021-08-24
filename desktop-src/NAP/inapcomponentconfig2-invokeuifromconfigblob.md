---
title: Méthode INapComponentConfig2 InvokeUIFromConfigBlob (NapCommon. h)
description: Est implémenté par les validateurs d’intégrité système (SHV) si nécessaire pour charger la configuration d’un ordinateur distant ou local en mémoire et afficher une interface utilisateur qui autorise la manipulation des données de configuration.
ms.assetid: 9c012690-6751-4a47-8683-74abac610c77
keywords:
- Méthode InvokeUIFromConfigBlob NAP
- Méthode InvokeUIFromConfigBlob NAP, interface INapComponentConfig2
- INapComponentConfig2 interface NAP, méthode InvokeUIFromConfigBlob
topic_type:
- apiref
api_name:
- INapComponentConfig2.InvokeUIFromConfigBlob
api_location:
- NapCommon.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 45d85e0506b8adf084b65a13a117a9dea3856fcff2e73f65a229bdb31b283fb9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119803159"
---
# <a name="inapcomponentconfig2invokeuifromconfigblob-method"></a>INapComponentConfig2 :: InvokeUIFromConfigBlob, méthode

> [!Note]  
> La plate-forme de protection d’accès réseau n’est pas disponible à partir de Windows 10

 

La méthode **InvokeUIFromConfigBlob** est implémentée par les validateurs d’intégrité système (SHV) si nécessaire pour charger la configuration d’un ordinateur distant ou local en mémoire et afficher une interface utilisateur qui permet de manipuler les données de configuration. Le composant de configuration doit prendre en charge l’utilisation de [**INapComponentConfig**](inapcomponentconfig.md) via DCOM.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT InvokeUIFromConfigBlob(
  [in, unique] HWND   hwndParent,
  [in]         UINT16 inbCount,
  [in]         BYTE   *inData,
  [out]        UINT16 *outbCount,
  [out]        BYTE   **outdata,
  [out]        BOOL   *fConfigChanged
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hwndParent* \[ dans\]
</dt> <dd>

Handle de la fenêtre parente ou propriétaire. Un handle de fenêtre valide doit être fourni.

</dd> <dt>

*inbCount* \[ dans\]
</dt> <dd>

Taille, en octets, des *indonnées*.

</dd> <dt>

*Indonnées* \[ dans\]
</dt> <dd>

Pointeur vers une mémoire tampon qui stocke les données de configuration initiales. Ces données sont exportées à partir de l’ordinateur distant ou local.

</dd> <dt>

*outbCount* \[ à\]
</dt> <dd>

Taille, en octets, des *données* de l’octet.

</dd> <dt>

*données* \[ de l' à\]
</dt> <dd>

Pointeur vers une mémoire tampon qui stocke les données de configuration modifiées par l’interface utilisateur de configuration SHV. Ces données sont importées par l’ordinateur distant ou local.

</dd> <dt>

*fConfigChanged* \[ à\]
</dt> <dd>

Pointeur vers un **booléen** dont la valeur est **true** si la configuration a été modifiée pendant l’opération d’interface utilisateur et **false** dans le cas contraire.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

retourne \_ la valeur OK si l’opération réussit ou l’un des codes d’erreur Windows standard.

## <a name="remarks"></a>Remarques

S’il est utilisé pour un ordinateur local, cette fonction peut être utilisée pour la configuration SHV de la stratégie. Il offre un moyen d’appeler une interface utilisateur SHV et de modifier une configuration SHV existante.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                     |
| En-tête<br/>                   | <dl> <dt>NapCommon. h</dt> </dl>   |
| MIDL<br/>                      | <dl> <dt>NapCommon. idl</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**INapComponentConfig2**](inapcomponentconfig2.md)
</dt> </dl>

 

 





