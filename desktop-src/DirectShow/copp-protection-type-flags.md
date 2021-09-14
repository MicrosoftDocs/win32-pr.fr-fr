---
description: Les constantes suivies sont utilisées avec le protocole de protection de sortie certifié (COPP) sur des mécanismes de protection de sortie spécifiques.
ms.assetid: a3cd63d8-22a5-473c-83c2-3499f3d32671
title: Indicateurs de type de protection COPP (DXVA. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COPP_ProtectionType_Unknown
- COPP_ProtectionType_None
- COPP_ProtectionType_HDCP
- COPP_ProtectionType_ACP
- COPP_ProtectionType_CGMSA
- COPP_ProtectionType_Mask
- COPP_ProtectionType_Reserved
api_type:
- HeaderDef
api_location:
- dxva.h
ms.openlocfilehash: 57e9ccc9420659ac09c19f2bbb7a18db519c07bc
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127111189"
---
# <a name="copp-protection-type-flags"></a>Indicateurs de type de protection COPP

Les constantes suivies sont utilisées avec le protocole de protection de sortie certifié (COPP) sur des mécanismes de protection de sortie spécifiques.



| Constante/valeur                                                                                                                                                                                                                                                                                                             | Description                                                     |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------|
| <span id="COPP_ProtectionType_Unknown"></span><span id="copp_protectiontype_unknown"></span><span id="COPP_PROTECTIONTYPE_UNKNOWN"></span><dl> <dt>**Copp \_ ProtectionType \_ inconnu**</dt> <dt>0x80000000</dt> </dl>     | Mécanisme de protection inconnu.<br/>                        |
| <span id="COPP_ProtectionType_None"></span><span id="copp_protectiontype_none"></span><span id="COPP_PROTECTIONTYPE_NONE"></span><dl> <dt>**Copp \_ ProtectionType \_ aucun**</dt> <dt>0x00000000</dt> </dl>                 | Aucun mécanisme de protection.<br/>                            |
| <span id="COPP_ProtectionType_HDCP"></span><span id="copp_protectiontype_hdcp"></span><span id="COPP_PROTECTIONTYPE_HDCP"></span><dl> <dt>**Copp \_ ProtectionType \_ HDCP**</dt> <dt>0x00000001</dt> </dl>                 | High-Bandwidth protection du contenu numérique (HDCP).<br/>    |
| <span id="COPP_ProtectionType_ACP"></span><span id="copp_protectiontype_acp"></span><span id="COPP_PROTECTIONTYPE_ACP"></span><dl> <dt>**Copp \_ ProtectionType \_ ACP**</dt> <dt>0x00000002</dt> </dl>                     | Protection contre la copie analogique (ACP).<br/>                        |
| <span id="COPP_ProtectionType_CGMSA"></span><span id="copp_protectiontype_cgmsa"></span><span id="COPP_PROTECTIONTYPE_CGMSA"></span><dl> <dt>**Copp \_ ProtectionType \_ CGMSA**</dt> <dt>0x00000004</dt> </dl>             | Version analogique du système de gestion de la génération de copie (CGMS-A).<br/> |
| <span id="COPP_ProtectionType_Mask"></span><span id="copp_protectiontype_mask"></span><span id="COPP_PROTECTIONTYPE_MASK"></span><dl> <dt>**Copp \_ ProtectionType \_ masque**</dt> <dt>0x80000007</dt> </dl>                 | Masque de masque pour isoler les indicateurs valides.<br/>                      |
| <span id="COPP_ProtectionType_Reserved"></span><span id="copp_protectiontype_reserved"></span><span id="COPP_PROTECTIONTYPE_RESERVED"></span><dl> <dt>**Copp \_ ProtectionType \_ réservé**</dt> <dt>0x7FFFFFF8</dt> </dl> | Réservé. Doit être zéro.<br/>                              |



## <a name="remarks"></a>Notes

Certaines méthodes retournent un seul indicateur à partir de ce type d’énumération, et certaines méthodes retournent une opération or au niveau du bit d' **un ou plusieurs** indicateurs.

Ces indicateurs sont utilisés dans les requêtes et les commandes COPP suivantes.

-   Niveau de protection global
-   Niveau de protection local
-   Type de protection
-   Définir le niveau de protection

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------|-----------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>DXVA. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Constantes et GUID](constants-and-guids.md)
</dt> <dt>

[Utilisation du protocole COPP (Certified Output Protection Protocol)](using-certified-output-protection-protocol--copp.md)
</dt> </dl>

 

 




