---
title: Méthode IVMDisplay SetDimensions (VPCCOMInterfaces. h)
description: Définit la hauteur et la largeur de l’affichage de la machine virtuelle, en pixels.
ms.assetid: 8ad5cfc4-59b4-4327-b088-d54adf9c6fda
keywords:
- Méthode SetDimensions Virtual PC
- Méthode SetDimensions Virtual PC, interface IVMDisplay
- IVMDisplay interface Virtual PC, méthode SetDimensions
topic_type:
- apiref
api_name:
- IVMDisplay.SetDimensions
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5bbf1db342342e9fbb8c0eff2df18f9c2a76443a4d20014bad34934ccecd3dfb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119473359"
---
# <a name="ivmdisplaysetdimensions-method"></a>IVMDisplay :: SetDimensions, méthode

\[Windows Virtual PC ne peut plus être utilisé à partir de Windows 8. Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Définit, en pixels, la hauteur et la largeur de l’affichage de la machine virtuelle.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT SetDimensions(
  [in] long displayPixelWidth,
  [in] long displayPixelHeight
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*displayPixelWidth* \[ dans\]
</dt> <dd>

Largeur, en pixels. La valeur doit être comprise entre les valeurs 640 et 2048. Si la valeur n’est pas divisible par 8, elle sera réduite au multiple de 8 inférieur suivant.

</dd> <dt>

*displayPixelHeight* \[ dans\]
</dt> <dd>

Hauteur, en pixels. La valeur doit être comprise entre les valeurs 480 et 1920.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode peut retourner l’une de ces valeurs.



| Code/valeur de retour                                                                                                                                                                    | Description                                                                                                                                                                                                      |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                                          | L'opération a réussi.<br/>                                                                                                                                                                         |
| <dl> <dt>**E \_ INVALIDARG**</dt> <dt>0x80000003</dt> </dl>                         | Le paramètre *displayPixelWidth* n’est pas divisible par 8, ou le paramètre *displayPixelWidth* ou *displayPixelHeight* est en dehors des valeurs minimales autorisées (640x480) ou 2048x1920).<br/> |
| <dl> <dt>**Ordinateur virtuel \_ E \_ a \_ expiré**</dt> <dt>0xA0040202</dt> </dl>                     | La modification de la résolution ne s’est pas terminée en temps opportun.<br/>                                                                                                                                              |
| <dl> <dt>**Ordinateur virtuel \_ \_Machine virtuelle \_ non \_ exécutée**</dt> <dt>0xA0040206</dt> </dl>               | L’ordinateur virtuel doit être en cours d’exécution pour cette opération.<br/>                                                                                                                                               |
| <dl> <dt>**Ordinateur virtuel \_ \_Machine virtuelle \_**</dt> <dt>0xA0040207</dt> inconnue </dl>                    | L’ordinateur virtuel n’est pas valide ou n’est pas en cours d’exécution.<br/>                                                                                                                                         |
| <dl> <dt>**Ordinateur virtuel \_ E \_ aucun \_**</dt> <dt>0xA0040850</dt> d’affichage </dl>                    | Impossible de trouver un affichage valide pour la machine virtuelle.<br/>                                                                                                                                                          |
| <dl> <dt>**Ordinateur virtuel \_ La \_ fonctionnalité d’ajouts E \_ \_ n’est pas disponible \_**</dt> <dt>0xA0040505</dt> </dl> | La version des composants d’intégration installés dans le système d’exploitation invité ne prend pas en charge cette opération.<br/>                                                                                    |
| <dl> <dt>**DISP \_ E \_ exception**</dt> <dt>0x80020009</dt> </dl>                    | Une erreur inattendue s’est produite.<br/>                                                                                                                                                                     |



 

## <a name="remarks"></a>Remarques

La taille minimale de l’affichage de l’ordinateur virtuel est de 640 x 480 pixels. La taille maximale est de 2048 x 1920. Toute tentative de définition de la taille d’affichage sur des valeurs en dehors de ces limites, ou sur une largeur qui n’est pas divisible par 8, entraîne le renvoi d’une erreur **E \_ INVALIDARG** .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | applications de \[ bureau Windows 7 uniquement\]<br/>                                                    |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                     |
| Fin de la prise en charge des clients<br/>    | Windows 7<br/>                                                                          |
| Produit<br/>                  | Windows Virtual PC<br/>                                                                 |
| En-tête<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMDisplay est défini en tant que 960895e9-f743-4498-96aa-261f867e7fc5<br/>                 |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IVMDisplay**](ivmdisplay.md)
</dt> </dl>

 

