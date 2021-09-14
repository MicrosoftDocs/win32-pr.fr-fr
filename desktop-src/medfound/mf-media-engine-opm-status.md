---
description: Définit l’état de Output Protection Manager (OPM).
ms.assetid: 7C4D88F6-369B-4364-90C4-6D0F8DD1523B
title: Énumération MF_MEDIA_ENGINE_OPM_STATUS
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MF_MEDIA_ENGINE_OPM_STATUS
api_type:
- HeaderDef
api_location:
- mfmediaengine.h
ms.openlocfilehash: 73585bf63bc559f30ce114730274e30518497b05
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127414182"
---
# <a name="mf_media_engine_opm_status-enumeration"></a>Énumération de l’état de l' \_ \_ \_ État OPM Media Engine \_

Définit l’état de [Output Protection Manager](output-protection-manager.md) (OPM).

## <a name="syntax"></a>Syntaxe


```C++
typedef enum _MF_MEDIA_ENGINE_OPM_STATUS { 
  MF_MEDIA_ENGINE_OPM_NOT_REQUESTED           =  0,
  MF_MEDIA_ENGINE_OPM_ESTABLISHED             = 1,
  MF_MEDIA_ENGINE_OPM_FAILED_VM               = 2,
  MF_MEDIA_ENGINE_OPM_FAILED_BDA              = 3,
  MF_MEDIA_ENGINE_OPM_FAILED_UNSIGNED_DRIVER  = 4,
  MF_MEDIA_ENGINE_OPM_FAILED                  = 5
} MF_MEDIA_ENGINE_OPM_STATUS;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="MF_MEDIA_ENGINE_OPM_NOT_REQUESTED"></span><span id="mf_media_engine_opm_not_requested"></span>**le \_ moteur multimédia MF \_ \_ OPM \_ n’est pas \_ demandé**
</dt> <dd>

État par défaut. Utilisé pour retourner l’état correct lorsque le contenu n’est pas protégé.

</dd> <dt>

<span id="MF_MEDIA_ENGINE_OPM_ESTABLISHED"></span><span id="mf_media_engine_opm_established"></span>**\_Media \_ Engine de \_ la \_ MF**
</dt> <dd>

OPM correctement établi.

</dd> <dt>

<span id="MF_MEDIA_ENGINE_OPM_FAILED_VM"></span><span id="mf_media_engine_opm_failed_vm"></span>**\_ \_ \_ machine virtuelle Media Engine OPM \_ ayant échoué \_**
</dt> <dd>

Échec de OPM en raison de l’exécution dans une machine virtuelle (VM).

</dd> <dt>

<span id="MF_MEDIA_ENGINE_OPM_FAILED_BDA"></span><span id="mf_media_engine_opm_failed_bda"></span>**échec de la \_ \_ OPM Media Engine \_ OPM \_ \_**
</dt> <dd>

Échec de OPM, car il n’existe aucun pilote graphique et le système utilise la carte d’affichage de base (BDA).

</dd> <dt>

<span id="MF_MEDIA_ENGINE_OPM_FAILED_UNSIGNED_DRIVER"></span><span id="mf_media_engine_opm_failed_unsigned_driver"></span>**\_ \_ \_ \_ \_ pilote non signé Media Engine OPM avec échec \_**
</dt> <dd>

Échec de OPM, car le pilote Graphics n’est pas PE signé, ce qui revient à WARP.

</dd> <dt>

<span id="MF_MEDIA_ENGINE_OPM_FAILED"></span><span id="mf_media_engine_opm_failed"></span>**\_échec de \_ OPM Media Engine \_ OPM \_**
</dt> <dd>

Échec de OPM pour d’autres raisons.

</dd> </dl>

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8.1 les \[ applications de bureau uniquement\]<br/>                                                 |
| Serveur minimal pris en charge<br/> | Windows Server 2012 \[Applications de bureau R2 uniquement\]<br/>                                      |
| MIDL<br/>                      | <dl> <dt>Mfmediaengine. idl</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Énumérations de Media Foundation](media-foundation-enumerations.md)
</dt> </dl>

 

 




