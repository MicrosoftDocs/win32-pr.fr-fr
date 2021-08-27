---
description: La structure NMEVENTDATA contient des informations sur une condition d’événement qui est transmise à Moniteur réseau pour insérer une ligne dans la visionneuse d’experts.
ms.assetid: 35cda410-d45a-4a51-91b7-8bd4a0c9957f
title: NMEVENTDATA, structure (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NMEVENTDATA
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: af2a4775be7d9e123974fbab865a8171d9bc9dec7dacae7692054bc6db0d3085
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120037039"
---
# <a name="nmeventdata-structure"></a>NMEVENTDATA, structure

La structure **NMEVENTDATA** contient des informations sur une condition d’événement qui est transmise à Moniteur réseau pour insérer une ligne dans la visionneuse d’experts.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct {
  BYTE         Version;
  DWORD        EventIdent;
  DWORD        Flags;
  DWORD        Severity;
  BYTE         NumColumns;
  LPSTR        szSourceName;
  LPSTR        szEventName;
  LPSTR        szDescription;
  LPSTR        szMachine;
  JTYPE        Justification;
  LPSTR        szUrl;
  SYSTEMTIME   SysTime;
  NMCOLUMNINFO Column[];
} NMEVENTDATA, *PNMEVENTDATA;
```



## <a name="members"></a>Membres

<dl> <dt>

**Version**
</dt> <dd>

Numéro de version de la structure **NMEVENTDATA** . Le numéro de version doit être égal à zéro. Les futures versions de Moniteur réseau peuvent prendre en charge un numéro de version plus élevé.

</dd> <dt>

**EventIdent**
</dt> <dd>

Identificateur de l’événement. **EventIdent** est unique pour chaque expert et référence une [page de référence d’événement](event-reference-page.md).

</dd> <dt>

**Indicateurs**
</dt> <dd>

Ensemble d’indicateurs qui décrit qui envoie les données d’événement et comment l’événement est affiché.



| Valeur                                                                                                                                                                                                                                              | Signification                                                                                                                                                                     |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="EVENT_FLAG_EXPERT"></span><span id="event_flag_expert"></span><dl> <dt>**\_expert en indicateurs d’événements \_**</dt> </dl>                                                                         | L’événement provient d’un expert. <br/>                                                                                                                                  |
| <span id="NMEVENTFLAG_DO_NOT_DISPLAY_SEVERITY"></span><span id="nmeventflag_do_not_display_severity"></span><dl> <dt>**NMEVENTFLAG \_ n' \_ affiche pas la \_ \_ gravité**</dt> </dl>                 | N’affiche pas le niveau de gravité de l’événement. <br/>                                                                                                                |
| <span id="NMEVENTFLAG_DO_NOT_DISPLAY_SOURCE"></span><span id="nmeventflag_do_not_display_source"></span><dl> <dt>**NMEVENTFLAG \_ n' \_ affiche pas la \_ \_ source**</dt> </dl>                       | N’affiche pas le nom de la source de l’événement. <br/>                                                                                                                   |
| <span id="NMEVENTFLAG_DO_NOT_DISPLAY_EVENT_NAME"></span><span id="nmeventflag_do_not_display_event_name"></span><dl> <dt>**NMEVENTFLAG \_ n' \_ affiche pas le nom de l' \_ \_ événement \_**</dt> </dl>          | N’affiche pas le nom de l’événement. <br/>                                                                                                                    |
| <span id="NMEVENTFLAG_DO_NOT_DISPLAY_DESCRIPTION"></span><span id="nmeventflag_do_not_display_description"></span><dl> <dt>**NMEVENTFLAG \_ ne \_ pas \_ afficher la \_ Description**</dt> </dl>        | N’affiche pas la description de l’événement. <br/>                                                                                                                   |
| <span id="NMEVENTFLAG_DO_NOT_DISPLAY_MACHINE"></span><span id="nmeventflag_do_not_display_machine"></span><dl> <dt>**NMEVENTFLAG \_ n' \_ affiche pas l' \_ \_ ordinateur**</dt> </dl>                    | N’affiche pas le nom de l’ordinateur pour l’événement. <br/>                                                                                                                  |
| <span id="NMEVENTFLAG_DO_NOT_DISPLAY_TIME"></span><span id="nmeventflag_do_not_display_time"></span><dl> <dt>**NMEVENTFLAG \_ n' \_ affiche pas l' \_ \_ heure**</dt> </dl>                             | Ne pas afficher l’heure de l’événement <br/>                                                                                                                           |
| <span id="NMEVENTFLAG_DO_NOT_DISPLAY_FIXED_COLUMNS"></span><span id="nmeventflag_do_not_display_fixed_columns"></span><dl> <dt>**NMEVENTFLAG \_ n' \_ \_ affiche pas \_ les \_ colonnes fixes**</dt> </dl> | N’affiche pas les colonnes gravité, source, nom de l’événement, description, machine ou heure. Il ne s’agit pas d’un indicateur unique, mais il s’agit d’une Union des six précédents indicateurs. <br/> |



 

</dd> <dt>

**Gravité**
</dt> <dd>

Niveau de gravité de l’événement. Le niveau de gravité peut avoir l’une des valeurs suivantes :

NMEVENT \_ Severity \_ information NMEVENT \_ gravité \_ Warning NMEVENT \_ gravité \_ Strong \_ Warning NMEVENT \_ gravité \_ erreur NMEVENT \_ gravité \_ grave \_ erreur NMEVENT \_ gravité \_ critique \_

</dd> <dt>

**NumColumns**
</dt> <dd>

Nombre de colonnes désignées dans la structure actuelle.

</dd> <dt>

**szSourceName**
</dt> <dd>

Nom de l’expert qui est affiché.

</dd> <dt>

**szEventName**
</dt> <dd>

Nom de l’événement qui est affiché.

</dd> <dt>

**szDescription**
</dt> <dd>

Description de l’événement qui s’affiche.

</dd> <dt>

**szMachine**
</dt> <dd>

Obsolète, doit avoir la **valeur null**.

</dd> <dt>

**Justification**
</dt> <dd>

Informations affichées dans la deuxième fenêtre du observateur d’événements. Le membre de **Justification** peut avoir la **valeur null**. Si la **valeur est null**, la deuxième fenêtre n’est pas visible.

</dd> <dt>

**szUrl**
</dt> <dd>

Réservé ce membre doit avoir la **valeur null**.

</dd> <dt>

**SysTime**
</dt> <dd>

Heure à laquelle la condition d’événement se produit. L’heure est mesurée par rapport au début de la capture.

</dd> <dt>

**Colonne**
</dt> <dd>

Tableau de structures de colonnes qui s’affiche dans le volet supérieur de la observateur d’événements.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                          |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                |
| En-tête<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



 

 




