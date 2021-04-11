---
title: Structure MPRESOURCE_INFO (MpClient. h)
description: Structure des informations sur les ressources.
ms.assetid: 2D645722-3DE3-4748-B532-3E522464EA1E
keywords:
- Fonctionnalités d’environnement Windows héritées de la structure MPRESOURCE_INFO
- PMPRESOURCE_INFO des fonctionnalités d’environnement Windows héritées du pointeur de structure
topic_type:
- apiref
api_name:
- MPRESOURCE_INFO
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dcac6552e0a0060df1bd6a0464fbb8f610395131
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942396"
---
# <a name="mpresource_info-structure"></a>\_Structure d’informations MPRESOURCE

Structure des informations sur les ressources.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct tagMPRESOURCE_INFO {
  MP_MIDL_STRING LPWSTR Scheme;
  MP_MIDL_STRING LPWSTR Path;
  MPRESOURCE_CLASS      Class;
} MPRESOURCE_INFO, *PMPRESOURCE_INFO;
```



## <a name="members"></a>Membres

<dl> <dt>

**Mode**
</dt> <dd>

Type : **MP \_ MIDL \_ String** de type LPWStr

</dd> <dd>

Identificateur de schéma de ressource tel que « file » ou « dir ».

</dd> <dt>

**Chemin d’accès**
</dt> <dd>

Type : **MP \_ MIDL \_ String** de type LPWStr

</dd> <dd>

Chemin d’accès absolu de la ressource, basé sur le **schéma**.

</dd> <dt>

**Classe**
</dt> <dd>

Type : **MPRESOURCE, \_ classe**

</dd> <dd>

Ce champ est défini lorsque la ressource est identifiée dans le cadre de la menace. Elle spécifie la classe de ressource, principalement concrète et latente. Il peut s’agir d’une combinaison de ces valeurs possibles :



| Valeur                                                                                                                                                                                                                                                                        | Signification                                                               |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| <span id="MP_RESOURCE_CLASS_UNKNOWN"></span><span id="mp_resource_class_unknown"></span><dl> Pack d’e <dt>**\_ Classe de ressources \_ \_ inconnue**</dt> <dt>0x0000</dt> </dl>              |                                                                       |
| <span id="MP_RESOURCE_CLASS_CONCRETE"></span><span id="mp_resource_class_concrete"></span><dl> Pack d’e <dt>**\_ Classe de ressources 0x0001 \_ \_ concrète**</dt> <dt></dt> </dl>           | S’exclut mutuellement avec la **\_ classe de ressource MP \_ \_ latente**.<br/>   |
| <span id="MP_RESOURCE_CLASS_LATENT"></span><span id="mp_resource_class_latent"></span><dl> Pack d’e <dt>**\_ Classe de ressource la0x0002 \_ \_ latente**</dt> <dt></dt> </dl>                 | S’exclut mutuellement avec la **\_ classe de ressources MP \_ \_ concrète**.<br/> |
| <span id="MP_RESOURCE_CLASS_SAMPLE_FILE"></span><span id="mp_resource_class_sample_file"></span><dl> Pack d’e <dt>**\_ \_Exemple de \_ \_ fichier de classe de ressources**</dt> <dt>0x0004</dt> </dl> |                                                                       |
| <span id="MP_RESOURCE_CLASS_SHARED"></span><span id="mp_resource_class_shared"></span><dl> Pack d’e <dt>**\_ 0x0100 \_ \_ partagé**</dt> de la classe de ressources <dt></dt> </dl>                 |                                                                       |



 

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 8 uniquement\]<br/>                                            |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2012 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>MpClient. h</dt> </dl> |



 

 





