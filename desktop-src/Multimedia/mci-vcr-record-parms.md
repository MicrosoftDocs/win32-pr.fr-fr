---
title: Structure de MCI_VCR_RECORD_PARMS (VCR. h)
description: La \_ structure de \_ paramètres d’enregistrement magnétoscope MCI \_ contient des paramètres pour la \_ commande d’enregistrement MCI pour les enregistreurs vidéo-cassettes.
ms.assetid: a95a6dab-9854-4c44-989a-032dff680106
keywords:
- structure MCI_VCR_RECORD_PARMS Windows multimédia
topic_type:
- apiref
api_name:
- MCI_VCR_RECORD_PARMS
api_location:
- Vcr.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4089b6b7977959b5eb0d0ac60dd4e612b17b823d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127195036"
---
# <a name="mci_vcr_record_parms-structure"></a>\_Structure des \_ PARMS des enregistrements magnétoscope MCI \_

La structure de paramètres d' **\_ \_ \_ enregistrement magnétoscope MCI** contient des paramètres pour la commande d' [**\_ enregistrement MCI**](mci-record.md) pour les enregistreurs vidéo-cassettes.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct tagMCI_VCR_RECORD_PARMS {
  DWORD_PTR dwCallback;
  DWORD     dwFrom;
  DWORD     dwTo;
  DWORD     dwAt;
} MCI_VCR_RECORD_PARMS;
```



## <a name="members"></a>Membres

<dl> <dt>

**dwCallback**
</dt> <dd>

Le mot de poids faible spécifie un handle de fenêtre utilisé pour l' \_ indicateur de notification MCI.

</dd> <dt>

**dwFrom**
</dt> <dd>

Position à partir de laquelle effectuer la lecture.

</dd> <dt>

**dwTo**
</dt> <dd>

Position de lecture.

</dd> <dt>

**dwAt**
</dt> <dd>

Valeur d’heure qui affecte [**l' \_ enregistrement MCI**](mci-record.md) ou la commande [**MCI \_ CUE**](mci-cue.md) . Pour **l' \_ enregistrement MCI**, il s’agit de l’heure de début de l’enregistrement. Pour **le \_ signal MCI**, il s’agit de l’heure à laquelle l’appareil de passage atteint la position donnée dans **dwFrom**.

</dd> </dl>

## <a name="remarks"></a>Notes

Les positions sont spécifiées dans le format d’heure actuel.

Lorsque vous assignez des données aux membres de cette structure, définissez les indicateurs correspondants dans le paramètre *fdwCommand* de la fonction [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) pour valider les membres.

## <a name="requirements"></a>Spécifications



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

[**\_signal MCI**](mci-cue.md)
</dt> <dt>

[**\_enregistrement MCI**](mci-record.md)
</dt> <dt>

[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))
</dt> </dl>

 

