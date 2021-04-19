---
description: La structure EXPERTENUMINFO fournit des informations sur l’expert.
ms.assetid: f745997b-d753-4c4d-88b6-6978f5eaa91c
title: EXPERTENUMINFO, structure (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EXPERTENUMINFO
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 35b8d36f55838492eb71640228d7216e6e594738
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106517448"
---
# <a name="expertenuminfo-structure"></a>EXPERTENUMINFO, structure

La structure **EXPERTENUMINFO** fournit des informations sur l’expert. Moniteur réseau alloue de la mémoire pour la structure et la transmet à l’expert lorsqu’il appelle la fonction d' [**expert d’inscription**](register-expert.md) . Lorsque l’expert reçoit la structure, il doit remplir toutes les informations que Moniteur réseau demandes.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct {
  char                szName[EXPERTSTRINGLENGTH];
  char                szVendor[EXPERTSTRINGLENGTH];
  char                szDescription[EXPERTSTRINGLENGTH];
  DWORD               Version;
  DWORD               Flags;
  HEXPERT             hExpert;
  char                szDllName[MAX_PATH];
  HINSTANCE           hModule;
  PEXPERTREGISTERPROC pRegisterProc;
  PEXPERTCONFIGPROC   pConfigProc;
  PEXPERTRUNPROC      pRunProc;
} EXPERTENUMINFO, *PEXPERTENUMINFO;
```



## <a name="members"></a>Membres

<dl> <dt>

**szName**
</dt> <dd>

Nom de l’expert.

</dd> <dt>

**szVendor**
</dt> <dd>

Nom du fournisseur qui crée l’expert.

</dd> <dt>

**szDescription**
</dt> <dd>

Description de l’expert. La valeur du membre **szDescription** peut être **null**. Si le nom est trop long, il est tronqué dans la configuration de la visionneuse par défaut.

</dd> <dt>

**Version**
</dt> <dd>

La valeur doit être égale à zéro.

</dd> <dt>

**Indicateurs**
</dt> <dd>

Les indicateurs suivants décrivent l’expert.



| Valeur                                                                                                                                                                                                                                                    | Signification                                                                                    |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| <span id="EXPERT_ENUM_FLAG_CONFIGURABLE"></span><span id="expert_enum_flag_configurable"></span><dl> <dt>**\_indicateur d’énumération expert \_ \_ configurable**</dt> </dl>                                          | L’expert prend en charge les appels à la méthode [**configure**](configure.md) . <br/>        |
| <span id="EXPERT_ENUM_FLAG_VIEWER_PRIVATE"></span><span id="expert_enum_flag_viewer_private"></span><dl> <dt>**\_visionneuse d’indicateurs d’énumération d’experts \_ \_ \_ privée**</dt> </dl>                                   | L’expert requiert un observateur d’événements privé (non partagé). <br/>                       |
| <span id="EXPERT_ENUM_FLAG_NO_VIEWER"></span><span id="expert_enum_flag_no_viewer"></span><dl> <dt>**\_ \_ visionneuse d’indicateur d’enum d' \_ expert \_**</dt> </dl>                                                  | L’expert n’envoie pas de notifications d’événements. <br/>                                  |
| <span id="EXPERT_ENUM_FLAG_ADD_ME_TO_RMC_IN_SUMMARY"></span><span id="expert_enum_flag_add_me_to_rmc_in_summary"></span><dl> <dt>**\_indicateur d’énumération expert \_ \_ ajouter \_ \_ à \_ RMC \_ en \_ Résumé**</dt> </dl> | Quand le focus se trouve dans le volet Résumé, l’expert s’affiche dans le menu contextuel. <br/> |
| <span id="EXPERT_ENUM_FLAG_ADD_ME_TO_RMC_IN_DETAIL"></span><span id="expert_enum_flag_add_me_to_rmc_in_detail"></span><dl> <dt>**\_indicateur d’énumération \_ d’experts \_ ajouter \_ \_ à \_ RMC \_ en \_ détail**</dt> </dl>    | Quand le focus se trouve dans le volet d’informations, l’expert s’affiche dans le menu contextuel. <br/>  |



 

</dd> <dt>

**hExpert**
</dt> <dd>

Handle vers l’expert. Lorsque la structure **EXPERTENUMINFO** est utilisée pour inscrire un expert, le paramètre est ignoré.

</dd> <dt>

**szDllName**
</dt> <dd>

Membre privé ; n’utilisez pas.

</dd> <dt>

**hModule**
</dt> <dd>

Membre privé ; n’utilisez pas.

</dd> <dt>

**pRegisterProc**
</dt> <dd>

Membre privé ; n’utilisez pas.

</dd> <dt>

**pConfigProc**
</dt> <dd>

Membre privé ; n’utilisez pas.

</dd> <dt>

**pRunProc**
</dt> <dd>

Membre privé ; n’utilisez pas.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                          |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                |
| En-tête<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



 

 




