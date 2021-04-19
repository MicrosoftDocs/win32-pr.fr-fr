---
title: IVMGuestOS IsHeartbeating, propriété (VPCCOMInterfaces. h)
description: Détermine si l’ordinateur virtuel a une pulsation.
ms.assetid: b1697a7b-6119-47aa-b261-6009f5287993
keywords:
- IsHeartbeating propriété Virtual PC
- IsHeartbeating, propriété Virtual PC, IVMGuestOS, interface
- IVMGuestOS interface Virtual PC, propriété IsHeartbeating
topic_type:
- apiref
api_name:
- IVMGuestOS.IsHeartbeating
- IVMGuestOS.get_IsHeartbeating
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: faad446749cbf3cdb75d6e8fa7469022cc004ea7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106510576"
---
# <a name="ivmguestosisheartbeating-property"></a>IVMGuestOS :: IsHeartbeating, propriété

\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8. Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Détermine si l’ordinateur virtuel a une pulsation.

Cette propriété est en lecture seule.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT get_IsHeartbeating(
  [out, retval] VARIANT_BOOL *heartBeating
);
```



## <a name="property-value"></a>Valeur de la propriété

**Variante \_ TRUE** si une pulsation est détectée **, \_ false** dans le cas contraire.

## <a name="error-codes"></a>Codes d’erreur



| Nom/valeur                                                                                                                                                              | Signification                                                                                                                                                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                                 | L'opération a réussi.<br/>                                                                                                                         |
| <dl> <dt>E \_ POINTEUR</dt> <dt>0x80004003</dt> </dl>                   | Le paramètre a la **valeur null**.<br/>                                                                                                                            |
| <dl> <dt>Ordinateur virtuel \_ \_Machine virtuelle \_ </dt> <dt>0xA0040207</dt> inconnue </dl>           | La configuration est inconnue.<br/>                                                                                                                         |
| <dl> <dt>Ordinateur virtuel \_ \_Machine virtuelle \_ non \_ exécutée</dt> <dt>0xA0040206</dt> </dl>      | L’ordinateur virtuel doit être en cours d’exécution pour cette opération.<br/>                                                                                               |
| <dl> <dt>Ordinateur virtuel \_ \_Ajouts \_ non \_ </dt> réalisés <dt>0xA0040504</dt> </dl> | L’ordinateur virtuel n’est pas entièrement démarré, la fonctionnalité composants d’intégration n’est pas installée ou la version installée ne prend pas en charge cette fonctionnalité.<br/> |
| <dl> <dt>DISP \_ E \_ exception</dt> <dt>0x80020009</dt> </dl>           | Une erreur inattendue s’est produite.<br/>                                                                                                                     |



## <a name="remarks"></a>Notes

Lorsque les composants d’intégration sont installés dans le système d’exploitation invité, un « battement » ou une pulsation standard est envoyé de la session de l’ordinateur virtuel vers Windows Virtual PC. Si le système d’exploitation invité est lourdement chargé, il est possible que Virtual PC reçoive moins de pulsations que prévu. Si aucune pulsation n’est détectée, il est possible que le système d’exploitation invité ne réponde pas ou soit bloqué.

Par défaut, un ordinateur virtuel produit dix cycles de pulsations par minute. Si aucune pulsation n’est détectée pendant une minute entière, Windows Virtual PC tente de redémarrer la session de l’ordinateur virtuel une fois toutes les dix secondes pendant une durée de deux minutes maximum. Ce comportement est contrôlé par les valeurs de clé suivantes dans le fichier de configuration de la session d’ordinateur virtuel.



| Clé de configuration                                            | Default       | Description                                                                                                                             |
|--------------------------------------------------------------|---------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| intégration/Microsoft/pulsation/heure<br/>              | 60<br/> | Longueur du bloc de temps utilisé pour générer des graduations de pulsations, en secondes.<br/>                                             |
| intégration/Microsoft/pulsation/taux<br/>              | 10<br/> | Nombre de graduations générées dans chaque bloc de temps de pulsation.<br/>                                                                  |
| intégration/Microsoft/pulsation/intervalle de défaillance \_<br/> | 10<br/> | Nombre de secondes entre les tentatives de redémarrage, une fois qu’aucun cycle de pulsation n’est reçu dans un bloc de temps de pulsation spécifique.<br/> |
| intégration/Microsoft/pulsations/échecs de \_ tentative<br/> | 12<br/> | Nombre de tentatives de redémarrage effectuées.<br/>                                                                                         |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 7 uniquement\]<br/>                                                    |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                     |
| Fin de la prise en charge des clients<br/>    | Windows 7<br/>                                                                          |
| Produit<br/>                  | Windows Virtual PC<br/>                                                                 |
| En-tête<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMGuestOS est défini en tant que 99fea0db-4880-499a-B6D8-73dff9bc91be<br/>                 |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IVMGuestOS**](ivmguestos.md)
</dt> </dl>

 

