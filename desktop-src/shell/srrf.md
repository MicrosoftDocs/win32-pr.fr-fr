---
description: Indicateurs qui limitent les données à définir ou à retourner.
title: SRRF (Shlwapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: c9dbffd1-3b3e-4a25-89ee-1666e2812a62
api_name:
- SRRF_RT_REG_NONE
- SRRF_RT_REG_SZ
- SRRF_RT_REG_EXPAND_SZ
- SRRF_RT_REG_BINARY
- SRRF_RT_REG_DWORD
- SRRF_RT_REG_MULTI_SZ
- SRRF_RT_REG_QWORD
- SRRF_RT_DWORD
- SRRF_RT_QWORD
- SRRF_RT_ANY
- SRRF_RM_ANY
- SRRF_RM_NORMAL
- SRRF_RM_SAFE
- SRRF_RM_SAFENETWORK
- SRRF_NOEXPAND
- SRRF_ZEROONFAILURE
- SRRF_NOVIRT
api_type:
- HeaderDef
api_location:
- Shlwapi.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 3ba36b64496413a54e6d8b8b96c16c265367d05c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104034668"
---
# <a name="srrf"></a>SRRF

Indicateurs qui limitent les données à définir ou à retourner.



| Constante/valeur                                                                                                                                                                                                                                           | Description                                                                                                                                                                                                            |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SRRF_RT_REG_NONE"></span><span id="srrf_rt_reg_none"></span><dl> <dt>**SRRF \_ RT \_ reg \_ None**</dt> <dt>0x00000001</dt> </dl>                 | Tapez REG \_ None.<br/>                                                                                                                                                                                             |
| <span id="SRRF_RT_REG_SZ"></span><span id="srrf_rt_reg_sz"></span><dl> <dt>**SRRF \_ RT \_ reg \_**</dt> <dt>0x00000002</dt> </dl>                       | Tapez REG \_ sz. \_ \_ Les types reg Expand SZ sont convertis automatiquement en reg \_ SZ, sauf si l' \_ indicateur NOEXPAND SRRF est spécifié.<br/>                                                                                     |
| <span id="SRRF_RT_REG_EXPAND_SZ"></span><span id="srrf_rt_reg_expand_sz"></span><dl> <dt>**SRRF \_ RT \_ reg \_ développer \_ SZ**</dt> <dt>0x00000004</dt> </dl> | Tapez REG \_ expand \_ sz. Si vous récupérez une valeur, vous devez également obtenir l' \_ indicateur NOEXPAND SRRF, ou [**SHRegGetValue**](/windows/desktop/api/Shlwapi/nf-shlwapi-shreggetvaluea) échoue avec le \_ paramètre error non valide \_ .<br/>                                     |
| <span id="SRRF_RT_REG_BINARY"></span><span id="srrf_rt_reg_binary"></span><dl> <dt>**SRRF \_ RT \_ reg \_ binaire**</dt> <dt>0x00000008</dt> </dl>           | Tapez REG \_ Binary.<br/>                                                                                                                                                                                           |
| <span id="SRRF_RT_REG_DWORD"></span><span id="srrf_rt_reg_dword"></span><dl> <dt>**SRRF \_ RT \_ reg ( \_ DWORD**</dt> ) <dt></dt> </dl>              | Tapez REG \_ DWORD.<br/>                                                                                                                                                                                            |
| <span id="SRRF_RT_REG_MULTI_SZ"></span><span id="srrf_rt_reg_multi_sz"></span><dl> <dt>**SRRF \_ RT \_ reg \_ multi- \_ SZ**</dt> <dt>0x00000020</dt> </dl>    | Tapez REG \_ multi \_ sz.<br/>                                                                                                                                                                                        |
| <span id="SRRF_RT_REG_QWORD"></span><span id="srrf_rt_reg_qword"></span><dl> <dt>**SRRF \_ RT \_ reg \_**</dt> <dt>0x00000040</dt> QWord </dl>              | Tapez REG \_ QWORD.<br/>                                                                                                                                                                                            |
| <span id="SRRF_RT_DWORD"></span><span id="srrf_rt_dword"></span><dl> <dt>**SRRF \_ RT \_ DWORD**</dt> <dt>0x00000018</dt> </dl>                           | \_Types de fichiers binaires reg DWORD et 32 bits \_ . Cette valeur est équivalente à SRRF \_ RT \_ reg \_ Binary \| SRRF \_ RT \_ reg reg \_ . Si vous récupérez une valeur, si les données binaires de la valeur sont supérieures à 32 bits, elles ne sont pas retournées.<br/> |
| <span id="SRRF_RT_QWORD"></span><span id="srrf_rt_qword"></span><dl> <dt>**SRRF \_ RT \_ QWord**</dt> <dt>0x00000048</dt> </dl>                           | \_Types de fichiers binaires reg QWord et 64 bits \_ . Cela équivaut à SRRF \_ RT \_ reg \_ Binary \| SRRF \_ RT \_ reg \_ QWORD. Si vous récupérez une valeur, si les données binaires de la valeur sont supérieures à 64 bits, elles ne sont pas retournées.<br/> |
| <span id="SRRF_RT_ANY"></span><span id="srrf_rt_any"></span><dl> <dt>**SRRF \_ RT \_ any**</dt> <dt>0x0000FFFF</dt> </dl>                                 | Tous les types. Définissez cet indicateur si aucune autre \_ valeur SRRF RT n’est définie.<br/>                                                                                                                                                 |
| <span id="SRRF_RM_ANY"></span><span id="srrf_rm_any"></span><dl> <dt>**SRRF \_ RM \_ n’importe quel**</dt> <dt>0x00000000</dt> </dl>                                 | Aucune restriction de mode. Il s’agit de la valeur par défaut.<br/>                                                                                                                                                             |
| <span id="SRRF_RM_NORMAL"></span><span id="srrf_rm_normal"></span><dl> <dt>**SRRF \_ 0x00010000 \_ normale RM**</dt> <dt></dt> </dl>                        | Limitez le mode de démarrage du système à « démarrage normal ».<br/>                                                                                                                                                              |
| <span id="SRRF_RM_SAFE"></span><span id="srrf_rm_safe"></span><dl> <dt>**SRRF \_ 0x00020000 \_ sécurisé RM**</dt> <dt></dt> </dl>                              | Limitez le mode de démarrage du système à « mode sans échec ».<br/>                                                                                                                                                                |
| <span id="SRRF_RM_SAFENETWORK"></span><span id="srrf_rm_safenetwork"></span><dl> <dt>**SRRF \_ RM \_ SAFENETWORK**</dt> <dt>0x00040000</dt> </dl>         | Limitez le mode de démarrage du système à « mode sans échec avec mise en réseau ».<br/>                                                                                                                                                |
| <span id="SRRF_NOEXPAND"></span><span id="srrf_noexpand"></span><dl> <dt>**SRRF \_ NOEXPAND**</dt> <dt>0x10000000</dt> </dl>                            | Ne développez pas automatiquement les chaînes d’environnement de REG \_ expand \_ sz.<br/>                                                                                                                                            |
| <span id="SRRF_ZEROONFAILURE"></span><span id="srrf_zeroonfailure"></span><dl> <dt>**SRRF \_ ZEROONFAILURE**</dt> <dt>0x20000000</dt> </dl>             | Si vous récupérez une valeur, si *pvData* n’est pas **null**, définissez le contenu de la mémoire tampon *pvData* sur tous les zéros en cas d’échec.<br/>                                                                                        |
| <span id="SRRF_NOVIRT"></span><span id="srrf_novirt"></span><dl> <dt>**SRRF \_ NOVIRT**</dt> <dt>0x40000000</dt> </dl>                                  | Lorsque vous récupérez une valeur, si la clé demandée est virtualisée, échec avec le fichier d’erreur \_ \_ \_ introuvable.<br/>                                                                                                            |



## <a name="remarks"></a>Notes

Ces valeurs sont définies dans Shlwapi. h.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                       |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                                 |
| En-tête<br/>                   | <dl> <dt>Shlwapi. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**SHRegSetValue**](/windows/desktop/api/shlwapi/nf-shlwapi-shregsetvalue)
</dt> <dt>

[**SHRegGetValue**](/windows/desktop/api/Shlwapi/nf-shlwapi-shreggetvaluea)
</dt> </dl>

 

 




