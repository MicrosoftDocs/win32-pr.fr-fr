---
description: Ces types de données peuvent être utilisés pour spécifier le type d’une valeur de registre.
title: Types de données de Registre (Winnt. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 4185e7af-e1f0-40af-91c7-0ff7e27896ae
api_name:
- REG_BINARY
- REG_DWORD
- REG_QWORD
- REG_DWORD_LITTLE_ENDIAN
- REG_QWORD_LITTLE_ENDIAN
- REG_DWORD_BIG_ENDIAN
- REG_EXPAND_SZ
- REG_LINK
- REG_MULTI_SZ
- REG_NONE
- REG_RESOURCE_LIST
- REG_SZ
api_type:
- HeaderDef
api_location:
- Winnt.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 4de4595b55716d58df04a598dd6ba298f22829d6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "104996592"
---
# <a name="registry-data-types"></a>Types de données de Registre

Ces types de données peuvent être utilisés pour spécifier le type d’une valeur de registre.



| Constante                                                                                                                                                                                      | Description                                                                                                                                                                                                                                                                                                                  |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="REG_BINARY"></span><span id="reg_binary"></span><dl> <dt>**\_fichier binaire reg**</dt> </dl>                                          | Données binaires dans tout formulaire.<br/>                                                                                                                                                                                                                                                                                          |
| <span id="REG_DWORD"></span><span id="reg_dword"></span><dl> <dt>**\_valeur DWORD reg**</dt> </dl>                                             | 32-nombre de bits.<br/>                                                                                                                                                                                                                                                                                                    |
| <span id="REG_QWORD"></span><span id="reg_qword"></span><dl> <dt>**\_q QWord**</dt> </dl>                                             | 64-nombre de bits.<br/>                                                                                                                                                                                                                                                                                                    |
| <span id="REG_DWORD_LITTLE_ENDIAN"></span><span id="reg_dword_little_endian"></span><dl> <dt>**REG \_ DWORD \_ Little \_ ENDIAN**</dt> </dl> | 32 bits au format avec primauté des octets de poids faible (Little endian). Cela équivaut à **reg \_ DWORD**.<br/> Au format Little endian, une valeur multioctet est stockée en mémoire à partir de l’octet le plus bas (le « petit end ») jusqu’à l’octet le plus élevé. Par exemple, la valeur 0x12345678 sinon est stockée sous la forme (0x78 0x56 0x34 0x12) au format avec primauté des octets de poids faible (Little endian).<br/> |
| <span id="REG_QWORD_LITTLE_ENDIAN"></span><span id="reg_qword_little_endian"></span><dl> <dt>**\_ \_ faible primauté des \_ octets de poids faible**</dt> </dl> | Nombre 64 bits au format avec primauté des octets de poids faible (Little endian). Cela équivaut à **reg \_ QWord**. <br/>                                                                                                                                                                                                                                   |
| <span id="REG_DWORD_BIG_ENDIAN"></span><span id="reg_dword_big_endian"></span><dl> <dt>**REG \_ DWORD \_ Big \_ ENDIAN**</dt> </dl>          | 32-nombre de bits au format Big-endian.<br/> Au format Big-endian, une valeur multioctet est stockée en mémoire à partir de l’octet le plus élevé (le « Big end ») jusqu’à l’octet le plus bas. Par exemple, la valeur 0x12345678 sinon est stockée sous la forme (0x12 0x34 0x56 0x78) au format Big-endian.<br/>                                                   |
| <span id="REG_EXPAND_SZ"></span><span id="reg_expand_sz"></span><dl> <dt>**REG \_ développer \_ SZ**</dt> </dl>                                | Chaîne terminée par le caractère null qui contient des références non développées à des variables d’environnement (par exemple, "% PATH%"). Il s’agit d’une chaîne Unicode ou ANSI, selon que vous utilisez les fonctions Unicode ou ANSI.<br/>                                                                                                     |
| <span id="REG_LINK"></span><span id="reg_link"></span><dl> <dt>**\_lien reg**</dt> </dl>                                                | Lien symbolique Unicode.<br/>                                                                                                                                                                                                                                                                                            |
| <span id="REG_MULTI_SZ"></span><span id="reg_multi_sz"></span><dl> <dt>**REG \_ multiple \_ SZ**</dt> </dl>                                   | Tableau de chaînes terminées par le caractère null qui se terminent par deux caractères null.<br/>                                                                                                                                                                                                                                      |
| <span id="REG_NONE"></span><span id="reg_none"></span><dl> <dt>**REG \_ aucun**</dt> </dl>                                                | Aucun type valeur défini.<br/>                                                                                                                                                                                                                                                                                            |
| <span id="REG_RESOURCE_LIST"></span><span id="reg_resource_list"></span><dl> <dt>**\_liste des ressources reg \_**</dt> </dl>                    | Liste des ressources de pilote de périphérique.<br/>                                                                                                                                                                                                                                                                                      |
| <span id="REG_SZ"></span><span id="reg_sz"></span><dl> <dt>**SZ de REG \_**</dt> </dl>                                                      | Chaîne terminée par un caractère Null. Il s’agit d’une chaîne Unicode ou ANSI, selon que vous utilisez les fonctions Unicode ou ANSI.<br/>                                                                                                                                                                                          |



## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------|------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>Winnt. h</dt> </dl> |



 

 




