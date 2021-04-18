---
title: Méthode IVMVirtualMachine AddHardDiskConnection (VPCCOMInterfaces. h)
description: Ajoute une nouvelle connexion de disque dur à la machine virtuelle.
ms.assetid: 0f4e0666-2cfd-4c73-884d-6f8b43186c05
keywords:
- Méthode AddHardDiskConnection Virtual PC
- Méthode AddHardDiskConnection Virtual PC, interface IVMVirtualMachine
- IVMVirtualMachine interface Virtual PC, méthode AddHardDiskConnection
topic_type:
- apiref
api_name:
- IVMVirtualMachine.AddHardDiskConnection
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0111577fd5cab614988e7295f3b8cdd59b8805c6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106512400"
---
# <a name="ivmvirtualmachineaddharddiskconnection-method"></a>IVMVirtualMachine :: AddHardDiskConnection, méthode

\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8. Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Ajoute une nouvelle connexion de disque dur à la machine virtuelle.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT AddHardDiskConnection(
  [in]          BSTR                  hardDiskPath,
  [in]          long                  busNumber,
  [in]          long                  deviceNumber,
  [out, retval] IVMHardDiskConnection **hardDiskConnection
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hardDiskPath* \[ dans\]
</dt> <dd>

Le chemin d’accès complet du fichier de disque dur virtuel (VHD) pour se connecter.

</dd> <dt>

*busNumber* \[ dans\]
</dt> <dd>

Bus auquel le lecteur sera attaché.



| Valeur                                                                        | Signification                                                  |
|------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <dt>0</dt> </dl> | Le lecteur sera attaché au premier bus.<br/>  |
| <dl> <dt>1</dt> </dl> | Le lecteur sera attaché au second bus.<br/> |



 

</dd> <dt>

*deviceNumber* \[ dans\]
</dt> <dd>

Appareil auquel le lecteur sera attaché.



| Valeur                                                                        | Signification                                                                |
|------------------------------------------------------------------------------|------------------------------------------------------------------------|
| <dl> <dt>0</dt> </dl> | Le lecteur sera attaché au premier périphérique sur le bus.<br/>  |
| <dl> <dt>1</dt> </dl> | Le lecteur sera attaché au deuxième périphérique sur le bus.<br/> |



 

</dd> <dt>

*hardDiskConnection* \[ out, retval\]
</dt> <dd>

Objet [**IVMHardDiskConnection**](ivmharddiskconnection.md) .

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode peut retourner l’une de ces valeurs.



| Code/valeur de retour                                                                                                                                                                              | Description                                                                                                                                               |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                                                    | L'opération a réussi.<br/>                                                                                                                  |
| <dl> <dt>**E \_ POINTEUR**</dt> <dt>0x80004003</dt> </dl>                                      | Le paramètre *hardDiskConnection* a la **valeur null**.<br/>                                                                                                |
| <dl> <dt>**E \_ INVALIDARG**</dt> <dt>0x80000003</dt> </dl>                                   | Un paramètre *hardDiskPath* a la **valeur null** ou le paramètre *busNumber* ou *deviceNumber* n’est pas valide.<br/>                                            |
| <dl> Valeur <dt>**HRESULT \_ FROM \_ Win32 ( \_ fichier d' \_ erreur \_ introuvable)**</dt> <dt>0x80070002</dt> </dl>   | Le système ne peut pas trouver le fichier spécifié par le paramètre *hardDiskPath* .<br/>                                                                     |
| <dl> Valeur <dt>**HRESULT \_ À partir de \_ Win32 ( \_ chemin d’erreur \_ \_ introuvable)**</dt> <dt>0x80070003</dt> </dl>   | Le système ne trouve pas le chemin d’accès spécifié par le paramètre *hardDiskPath* .<br/>                                                                     |
| <dl> Valeur <dt>**HRESULT \_ À partir de \_ Win32 (erreur \_ \_ nom non valide)**</dt> <dt>0x8007007b</dt> </dl>      | Le paramètre *hardDiskPath* contient un caractère non valide (l’un des caractères \* suivants : «  ? <>/ \| » :»).<br/>                                                        |
| <dl> Valeur <dt>**HRESULT \_ FROM \_ Win32 (erreur \_ de \_ nom de chemin incorrect)**</dt> <dt>0x800700a1</dt> </dl>      | Le paramètre *hardDiskPath* spécifie un chemin d’accès vide ou relatif. Un chemin d’accès absolu est requis.<br/>                                                |
| <dl> Valeur <dt>**HRESULT \_ À partir de \_ Win32 \_ ( \_ dépassement de mémoire tampon d’erreur)**</dt> <dt>0x8007006f</dt> </dl>   | Le chemin d’accès spécifié par le paramètre *hardDiskPath* est trop long. Le chemin d’accès doit être inférieur à 260 caractères.<br/>                                     |
| <dl> <dt>**Ordinateur virtuel \_ \_Machine virtuelle \_**</dt> <dt>0xA0040207</dt> inconnue </dl>                              | La configuration est inconnue.<br/>                                                                                                                  |
| <dl> <dt>**Ordinateur virtuel \_ \_Machine virtuelle \_ en cours d’exécution \_ ou \_**</dt> <dt>0xA004020B</dt> </dl>                   | L’ordinateur virtuel est dans un État en cours d’exécution ou enregistré.<br/>                                                                                                         |
| <dl> <dt>**Ordinateur virtuel \_ 0xA00400503 \_ \_ de bus \_ de lecteur E \_ en cours d' \_ utilisation**</dt> <dt></dt> </dl>                | L’emplacement de bus spécifié est en cours d’utilisation.<br/>                                                                                                          |
| <dl> <dt>**Ordinateur virtuel \_ E \_ \_ \_ fichier HD 0xA0040682 non valide**</dt> <dt></dt> </dl>                        | Le disque dur virtuel est supérieur à 127 Go et ne peut pas être connecté au bus IDE.<br/>                                                                         |
| <dl> <dt>**Ordinateur virtuel \_ E \_ \_ \_ \_ type de disque HD non pris en charge**</dt> <dt>0xA00400686</dt> </dl>             | Le paramètre *hardDiskPath* fait référence à un disque dur virtuel lié ou à un disque dur virtuel de différenciation sur un disque dur virtuel lié. Les disques durs virtuels liés ne peuvent pas être attachés aux machines virtuelles.<br/> |
| <dl> Valeur <dt>**HRESULT \_ À partir de \_ Win32 \_ ( \_ violation de partage d’erreur)**</dt> <dt>0x80070020</dt> </dl> | Le disque dur virtuel spécifié est déjà connecté à un autre emplacement de bus pour cette machine virtuelle.<br/>                                                                    |
| <dl> <dt>**DISP \_ E \_ exception**</dt> <dt>0x80020009</dt> </dl>                              | Une erreur inattendue s’est produite.<br/>                                                                                                              |



 

## <a name="remarks"></a>Notes

Vous pouvez uniquement ajouter une nouvelle connexion de disque dur à une machine virtuelle arrêtée.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 7 uniquement\]<br/>                                                    |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                     |
| Fin de la prise en charge des clients<br/>    | Windows 7<br/>                                                                          |
| Produit<br/>                  | Windows Virtual PC<br/>                                                                 |
| En-tête<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMVirtualMachine est défini en tant que f7092aa1-33ed-4f78-a59f-c00adfc2edd7<br/>          |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IVMVirtualMachine**](ivmvirtualmachine.md)
</dt> </dl>

 

