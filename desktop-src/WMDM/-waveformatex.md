---
title: Structure _WAVEFORMATEX
description: La structure \_WAVEFORMATEX définit le format des données audio .wav.
ms.assetid: 2128f07a-4858-49b7-b031-16d4a84c9d32
keywords:
- Structure de _WAVEFORMATEX Windows Media Gestionnaire de périphériques
topic_type:
- apiref
api_name:
- _WAVEFORMATEX
api_location:
- wmdm.idl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e149608d740df6df40b39b64b09ac11837a721b5b4844f1a73eb52e1b5cea479
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118586744"
---
# <a name="_waveformatex-structure"></a>\_WAVEFORMATEX, structure

La structure **\_ WAVEFORMATEX** définit le format des données Waveform-Audio.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct _tWAVEFORMATEX {
  WORD  wFormatTag;
  WORD  nChannels;
  DWORD nSamplesPerSec;
  DWORD nAvgBytesPerSec;
  WORD  nBlockAlign;
  WORD  wBitsPerSample;
  WORD  cbSize;
} _WAVEFORMATEX;
```



## <a name="members"></a>Membres

<dl> <dt>

**wFormatTag**
</dt> <dd>

Doit être défini avec un format ou des formats pris en charge par l’appareil. notez que les versions précédentes du Windows Media Gestionnaire de périphériques recommandé avec WMDM \_ WAVE \_ FORMAT \_ all pour indiquer la prise en charge de tous les formats. Toutefois, cela n’est plus recommandé, car les différents lecteurs multimédias interprètent cela de différentes manières, et quelques appareils peuvent véritablement lire n’importe quel format de fichier. Il est maintenant recommandé d’utiliser les valeurs valides de l’énumération WMDM d’énumération \_ \_ \_ \_ \_ n’importe quelle valeur de l’énumération des [**\_ \_ \_ \_ \_ valeurs valides**](wmdm-enum-prop-valid-values-form.md) de l’énumération WMDM, ou de mieux spécifier une plage de formats avec la structure de la [**plage des valeurs de WMDM \_ prop \_ \_**](wmdm-prop-values-range.md) .

</dd> <dt>

**nChannels**
</dt> <dd>

Nombre de canaux dans les données audio Waveform. Les données mono utilisent un canal et les données stéréo utilisent deux canaux.

</dd> <dt>

**nSamplesPerSec**
</dt> <dd>

Taux d’échantillonnage, en échantillons par seconde (Hertz), auquel chaque canal doit être lu ou enregistré. Les valeurs courantes pour **nSamplesPerSec** sont 8,0 kilohertz (kHz), 11,025 khz, 22,05 khz et 44,1 kHz.

</dd> <dt>

**nAvgBytesPerSec**
</dt> <dd>

Taux moyen de transfert de données requis pour la balise format, en octets par seconde. Les logiciels de lecture et d’enregistrement peuvent estimer la taille des mémoires tampons à l’aide du membre **nAvgBytesPerSec** .

</dd> <dt>

**nBlockAlign**
</dt> <dd>

Alignement de bloc, en octets. L’alignement de bloc est l’unité atomique minimale des données pour le type de format **wFormatTag** . Le logiciel de lecture et d’enregistrement doit traiter un multiple de **nBlockAlign** octets de données à la fois. Les données écrites et lues à partir d’un appareil doivent toujours commencer au début d’un bloc. Par exemple, il n’est pas possible de démarrer correctement les données PCM au milieu d’un échantillon (autrement dit, sur une limite qui n’est pas alignée de bloc).

</dd> <dt>

**wBitsPerSample**
</dt> <dd>

Bits par échantillon pour le type de format **wFormatTag** .

</dd> <dt>

**cbSize**
</dt> <dd>

Ce membre est ignoré.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|-------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>WMDM. idl</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IMDSPDevice::GetFormatSupport**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspdevice-getformatsupport)
</dt> <dt>

[**IMDSPStorage::CreateStorage**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspstorage-createstorage)
</dt> <dt>

[**IMDSPStorage :: GetAttributes**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspstorage-getattributes)
</dt> <dt>

[**IWMDMDevice::GetFormatSupport**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice-getformatsupport)
</dt> <dt>

[**IWMDMOperation::GetObjectAttributes**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmoperation-getobjectattributes)
</dt> <dt>

[**IWMDMOperation::SetObjectAttributes**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmoperation-setobjectattributes)
</dt> <dt>

[**IWMDMStorage :: GetAttributes**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage-getattributes)
</dt> <dt>

[**Structures**](structures.md)
</dt> </dl>

 

 





