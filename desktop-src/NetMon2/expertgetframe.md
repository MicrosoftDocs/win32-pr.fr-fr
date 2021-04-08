---
description: Retourne le frame demandé à partir d’une capture chargée.
ms.assetid: efd1cff5-a3a1-4910-b003-25b6e10dad6e
title: ExpertGetFrame, fonction (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ExpertGetFrame
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 2bd02bde8caf157b6df6b1dd772a8f7574df0e57
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862021"
---
# <a name="expertgetframe-function"></a>ExpertGetFrame fonction)

La fonction **ExpertGetFrame** retourne le frame demandé à partir d’une capture chargée.

## <a name="syntax"></a>Syntaxe


```C++
DWORD WINAPI ExpertGetFrame(
  _In_  HEXPERTKEY              hExpertKey,
  _In_  DWORD                   Direction,
  _In_  DWORD                   RequestFlags,
  _In_  DWORD                   RequestedFrameNumber,
  _In_  HFILTER                 hFilter,
  _Out_ LPEXPERTFRAMEDESCRIPTOR pEFrameDescriptor
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hExpertKey* \[ dans\]
</dt> <dd>

Identificateur d’expert unique. Moniteur réseau transmet l’identificateur *hExpertKey* à l’expert lorsqu’il appelle la fonction [**Run**](run.md) .

</dd> <dt>

*Sens* \[ dans\]
</dt> <dd>

Valeur qui identifie la façon dont Moniteur réseau recherche le frame.



| Valeur                                                                                                                                                                                         | Signification                                |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------|
| <span id="GET_SPECIFIED_FRAME"></span><span id="get_specified_frame"></span><dl> <dt>**Obtient \_ le \_ Frame spécifié**</dt> </dl>              | Retourne le frame demandé.<br/> |
| <span id="GET_FRAME_NEXT_FORWARD"></span><span id="get_frame_next_forward"></span><dl> <dt>**RECEVOIR le \_ cadre \_ suivant \_**</dt> </dl>    | Retourne le frame suivant.<br/>      |
| <span id="GET_FRAME_NEXT_BACKWARD"></span><span id="get_frame_next_backward"></span><dl> <dt>**RECEVOIR le frame vers l' \_ \_ \_ arrière suivant**</dt> </dl> | Retourne le frame précédent.<br/>  |



 

</dd> <dt>

*RequestFlags* \[ dans\]
</dt> <dd>

Indicateurs qui spécifient comment Moniteur réseau doit gérer la requête. Spécifiez un ou plusieurs des indicateurs suivants.



| Valeur                                                                                                                                                                                             | Signification                                                                                                                                                                                                                                                                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="FLAGS_DEFER_TO_UI_FILTER"></span><span id="flags_defer_to_ui_filter"></span><dl> <dt>**les indicateurs \_ diffèrent \_ du \_ filtre d’interface utilisateur \_**</dt> </dl> | Avant d’appliquer le paramètre de filtre d’affichage de l’expert qui est spécifié dans *hFilter*, appliquez le filtre d’affichage que Moniteur réseau utilise au démarrage de l’expert.<br/>                                                                                                                              |
| <span id="FLAGS_ATTACH_PROPERTIES"></span><span id="flags_attach_properties"></span><dl> <dt>**INDICATEURS \_ propriétés d’attachement \_**</dt> </dl>      | Les propriétés que tous les analyseurs de protocole localisent avec les sections revendiquées de ce frame sont attachées au frame. Si l’indicateur n’est pas défini, le champ **lpPropertyTable** de la structure [**EXPERTFRAMEDESCRIPTOR**](expertframedescriptor.md) (retournée par **PEFrameDescriptor**) aura la valeur **null**.<br/> |



 

</dd> <dt>

*RequestedFrameNumber* \[ dans\]
</dt> <dd>

Numéro de la trame demandée.

</dd> <dt>

*hFilter* \[ dans\]
</dt> <dd>

Handle vers le filtre d’affichage de l’expert. Si l’expert n’a pas de filtre d’affichage, affectez la valeur **null** au paramètre.

</dd> <dt>

*pEFrameDescriptor* \[ à\]
</dt> <dd>

La structure [**EXPERTFRAMEDESCRIPTOR**](expertframedescriptor.md) qui, au retour, décrit le frame. L’expert doit allouer et libérer la mémoire utilisée par cette structure.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la fonction réussit, la valeur de retour est NMERR \_ Success.

Si la fonction échoue, la valeur de retour indique la raison de l’échec. Si la valeur de retour est NMERR \_ expert \_ Terminate, l’expert doit immédiatement procéder au nettoyage et au retour ; l’utilisateur a annulé l’exécution de l’expert.

## <a name="remarks"></a>Notes

Si vous définissez FLAGs \_ Attach \_ Properties, l’appel nécessite plus de ressources que si vous ne définissez pas l’indicateur. Si l’indicateur n’est pas défini, un pointeur pointe vers le frame brut et vers les données relatives au frame. Si cet indicateur est défini, Moniteur réseau joint toutes les propriétés au frame en appelant chaque analyseur qui prétend une partie du frame. Il peut s’agir d’un processus lent.

Les experts ne doivent pas définir \_ l' \_ indicateur de propriétés d’attachement Flags, sauf si les experts requièrent les propriétés que les analyseurs attachent au frame. Si possible, les experts doivent appeler la fonction **ExpertGetFrame** sans l’indicateur, puis extraire les données requises directement à partir du frame.

Si l’expert appelle **ExpertGetFrame** sans l’indicateur Flags \_ Attach \_ Properties et requiert les propriétés associées à ce frame (un événement, par exemple), l’expert appelle **ExpertGetFrame** avec les mêmes paramètres, à l’exception des éléments suivants :

``` syntax
Direction = EXPERT_GET_SPECIFIED_FRAME;
RequestFlags &= (~EXPERT_DEFER_TO_UI_FILTER) | EXPERT_ATTACH_PROPERTIES;
RequestedFrameNumber= (The actual frame number you want);
hFilter = NULL;
pEFrameDescriptor = (The same one as last time);
```

L’utilisation du code précédent garantit que l’expert obtient le frame requis sans devoir rappeler le code de filtre.

Vous pouvez définir le paramètre *hFilter* en tant que **LPVOID**. S’il existe, le frame retourné passe ce filtre. Si l’expert n’a pas de filtre d’affichage à passer à la fonction (si *hFilter* a la **valeur null** ), le frame retourné n’est pas filtré.

La fonction **ExpertGetFrame** peut uniquement être appelée par des experts qui implémentent la fonction [**exécuter**](run.md) ou [**configurer**](configure.md) l’exportation.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                           |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                 |
| En-tête<br/>                   | <dl> <dt>Netmon. h</dt> </dl>  |
| Bibliothèque<br/>                  | <dl> <dt>Nmapi. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




