---
title: Structure de MCI_VCR_STEP_PARMS (VCR. h)
description: La structure de l' \_ \_ étape de magnétoscope MCI contient des \_ paramètres pour la \_ commande d’étape MCI pour les enregistreurs vidéo-cassettes.
ms.assetid: 57751de6-d174-418f-8167-402d3ead4e24
keywords:
- structure MCI_VCR_STEP_PARMS Windows multimédia
topic_type:
- apiref
api_name:
- MCI_VCR_STEP_PARMS
api_location:
- Vcr.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7f25e79903a694b6537e88d1c58994d1f39ccf958ea95f40f571a267239a055e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119783827"
---
# <a name="mci_vcr_step_parms-structure"></a>\_Étape de \_ \_ gestion des magnétoscopes MCI

La structure de l' **\_ étape de magnétoscope \_ \_ MCI** contient des paramètres pour la commande d' [**\_ étape MCI**](mci-step.md) pour les enregistreurs vidéo-cassettes.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct tagMCI_VCR_STEP_PARMS {
  DWORD_PTR dwCallback;
  DWORD     dwFrames;
} MCI_VCR_STEP_PARMS;
```



## <a name="members"></a>Membres

<dl> <dt>

**dwCallback**
</dt> <dd>

Le mot de poids faible spécifie un handle de fenêtre utilisé pour l' \_ indicateur de notification MCI.

</dd> <dt>

**dwFrames**
</dt> <dd>

Nombre de frames à sauter (longueur d’une seule étape) à mesure que la commande d' [**\_ étape MCI**](mci-step.md) progresse vers l’avant ou vers l’arrière dans le contenu.

</dd> </dl>

## <a name="remarks"></a>Remarques

Lorsque vous assignez des données aux membres de cette structure, définissez les indicateurs correspondants dans le paramètre *fdwCommand* de [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) pour valider les membres.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                       |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                             |
| En-tête<br/>                   | <dl> <dt>VCR. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**MCI**](mci.md)
</dt> <dt>

[**Structures MCI**](mci-structures.md)
</dt> <dt>

[**\_étape MCI**](mci-step.md)
</dt> <dt>

[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))
</dt> </dl>

 

