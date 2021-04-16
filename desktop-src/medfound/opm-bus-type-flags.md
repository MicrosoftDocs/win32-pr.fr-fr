---
description: Les indicateurs figurant dans le tableau ci-dessous spécifient le type de bus d’e/s utilisé par la carte graphique.
ms.assetid: 6c8ec020-5f12-453b-bbeb-3baabb1ca213
title: Indicateurs de type de bus OPM (Opmapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae3e6988d6bcd33015b0efc5b12561ef3373a9e8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527892"
---
# <a name="opm-bus-type-flags"></a>Indicateurs de type de bus OPM

Les indicateurs figurant dans le tableau ci-dessous spécifient le type de bus d’e/s utilisé par la carte graphique.



| Constante/valeur                                                                                                                                                                                                                                                                                                                                                                                                      | Description                                                                                                                                                                                                                                                                                                                                                                                |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="OPM_BUS_TYPE_OTHER"></span><span id="opm_bus_type_other"></span><dl> <dt>**OPM \_ TYPE de BUS \_ \_ autre**</dt> <dt>0x00000000</dt> </dl>                                                                                                                                                                      | Indique un type de bus autre que les types répertoriés ici.<br/>                                                                                                                                                                                                                                                                                                                       |
| <span id="OPM_BUS_TYPE_PCI"></span><span id="opm_bus_type_pci"></span><dl> <dt>**OPM \_ TYPE de BUS \_ \_ PCI**</dt> <dt>0x00000001</dt> </dl>                                                                                                                                                                            | Bus PCI.<br/>                                                                                                                                                                                                                                                                                                                                                                        |
| <span id="OPM_BUS_TYPE_PCIX"></span><span id="opm_bus_type_pcix"></span><dl> <dt>**OPM \_ TYPE de BUS \_ \_ PCIx**</dt> <dt>0x00000002</dt> </dl>                                                                                                                                                                         | Bus PCI-X.<br/>                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="OPM_BUS_TYPE_PCIEXPRESS"></span><span id="opm_bus_type_pciexpress"></span><dl> <dt>**OPM \_ TYPE de BUS \_ \_ PCIEXPRESS**</dt> <dt>0x00000003</dt> </dl>                                                                                                                                                       | Bus PCI Express.<br/>                                                                                                                                                                                                                                                                                                                                                                |
| <span id="OPM_BUS_TYPE_AGP"></span><span id="opm_bus_type_agp"></span><dl> <dt>**OPM \_ TYPE de BUS \_ \_ AGP**</dt> <dt>0x00000004</dt> </dl>                                                                                                                                                                            | Bus AGP (Accelerated Graphics Port).<br/>                                                                                                                                                                                                                                                                                                                                            |
| <span id="OPM_BUS_IMPLEMENTATION_MODIFIER_INSIDE_OF_CHIPSET"></span><span id="opm_bus_implementation_modifier_inside_of_chipset"></span><dl> <dt>**OPM \_ \_ \_ Modificateur d’implémentation \_ de bus à l’intérieur \_ d’un \_ Chipset**</dt> <dt>0x00010000</dt> </dl>                                                                      | L’implémentation de la carte graphique se trouve dans le pont nord d’un chipset de carte mère. Cet indicateur implique que les données ne sont jamais placées sur un bus d’expansion (comme PCI ou AGP) lorsqu’elles sont transférées de la mémoire principale vers la carte graphique. <br/>                                                                                                                                     |
| <span id="OPM_BUS_IMPLEMENTATION_MODIFIER_TRACKS_ON_MOTHER_BOARD_TO_CHIP"></span><span id="opm_bus_implementation_modifier_tracks_on_mother_board_to_chip"></span><dl> <dt>**OPM \_ \_ \_ Le modificateur d’implémentation \_ de bus effectue \_ le suivi de la \_ carte mère \_ \_ \_**</dt> sur la puce <dt>0x00020000</dt> </dl>                            | La carte graphique est connectée au pont nord d’un chipset de carte mère par des pistes sur la carte mère, et toutes les puces de la carte graphique (circuits intégrés) sont soudées à la carte mère. <br/>                                                                                                                                                                         |
| <span id="OPM_BUS_IMPLEMENTATION_MODIFIER_TRACKS_ON_MOTHER_BOARD_TO_SOCKET"></span><span id="opm_bus_implementation_modifier_tracks_on_mother_board_to_socket"></span><dl> <dt>**OPM \_ \_ \_ Le modificateur \_ d’implémentation de bus effectue \_ le suivi de la \_ carte mère sur le \_ \_ \_ Socket**</dt> <dt>0x00030000</dt> </dl>                      | La carte graphique est connectée au pont nord d’un chipset de carte mère par des pistes sur la carte mère, et toutes les puces de la carte graphique sont connectées via des sockets à la carte mère.<br/>                                                                                                                                                                               |
| <span id="OPM_BUS_IMPLEMENTATION_MODIFIER_DAUGHTER_BOARD_CONNECTOR"></span><span id="opm_bus_implementation_modifier_daughter_board_connector"></span><dl> <dt>**OPM \_ Connecteur de la \_ \_ \_ \_ carte \_ fille du modificateur d’implémentation du bus**</dt> <dt>0x00040000</dt> </dl>                                                 | La carte graphique est connectée à la carte mère via un connecteur en fille.<br/>                                                                                                                                                                                                                                                                                         |
| <span id="OPM_BUS_IMPLEMENTATION_MODIFIER_DAUGHTER_BOARD_CONNECTOR_INSIDE_OF_NUAE"></span><span id="opm_bus_implementation_modifier_daughter_board_connector_inside_of_nuae"></span><dl> <dt>**OPM \_ \_ \_ \_ \_ Connecteur de carte fille du modificateur \_ d’implémentation de bus \_ dans \_ \_ NUAE**</dt> <dt>0x00050000</dt> </dl> | La carte graphique est connectée à la carte mère via un connecteur à fille et la carte graphique est à l’intérieur d’un boîtier qui n’est pas accessible par l’utilisateur.<br/>                                                                                                                                                                                                            |
| <span id="OPM_BUS_IMPLEMENTATION_MODIFIER_NON_STANDARD"></span><span id="opm_bus_implementation_modifier_non_standard"></span><dl> <dt>**OPM \_ \_Modificateur d’implémentation de bus \_ \_ non \_ standard**</dt> <dt>0x80000000</dt> </dl>                                                                                      | Modificateur non standard. (Facultatif.)<br/>                                                                                                                                                                                                                                                                                                                                               |
| <span id="OPM_COPP_COMPATIBLE_BUS_TYPE_INTEGRATED"></span><span id="opm_copp_compatible_bus_type_integrated"></span><dl> <dt>**OPM \_ \_Type de bus compatible Copp à l' \_ \_ \_ intégration**</dt> <dt>0x80000000</dt> </dl>                                                                                                     | Bus intégré. Cet indicateur est utilisé uniquement en mode d’émulation COPP. Elle indique que la commande et le signal d’État entre la carte graphique et les autres sous-systèmes de l’ordinateur ne sont pas disponibles sur un bus d’extension qui a une spécification publique et un type de connecteur standard, sauf s’il s’agit d’un bus de mémoire. Cet indicateur peut être combiné avec un indicateur de **\_ type bus OPM \_ \_ xxx** .<br/> |



## <a name="remarks"></a>Notes

Jusqu’à trois indicateurs peuvent être définis à l’aide d' **une opération or** au niveau du bit. Les indicateurs de la plage 0x00 à 0x04 **( \_ type de bus OPM \_ \_ xxx**) donnent le type de bus de base. Les indicateurs dans la plage 0x10000 à 0x50000 **( \_ \_ \_ modificateur d’implémentation \_ de bus OPM xxx**) modifient la description de base. Le pilote définit un indicateur de type bus et peut éventuellement avoir la valeur d’un indicateur de modificateur. En outre, le pilote peut éventuellement définir l’indicateur **\_ \_ \_ \_ non \_ standard du modificateur d’implémentation de bus OPM** .

En mode d’émulation COPP, le pilote n’utilise pas les indicateurs de modificateur, mais il peut définir l’indicateur **\_ intégré de \_ \_ \_ type \_ de bus compatible OPM Copp** .

Les \_ \_ indicateurs de type de bogue OPM \_ xxxx et le **\_ \_ \_ \_ type de \_ bus compatible OPM Copp** sont équivalents aux valeurs de l’énumération [**Copp \_ BusType**](/windows/win32/api/dxva9typ/ne-dxva9typ-copp_bustype) utilisées dans le protocole Copp (Certified Output Protection Protocol).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                      |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                                |
| En-tête<br/>                   | <dl> <dt>Opmapi. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Énumérations OPM](opm-enumerations.md)
</dt> </dl>

 

 
