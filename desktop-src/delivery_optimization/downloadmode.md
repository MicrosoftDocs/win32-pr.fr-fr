---
title: Énumération DownloadMode (Deliveryoptimization. h)
description: Définit les différents modes de téléchargement utilisés par l’optimisation de la distribution.
ms.assetid: 7E9407C6-A22F-459E-B316-5E7809F0067A
keywords:
- Permet de contourner l’optimisation de la distribution et d’utiliser la fonction BITS, à la place. Par exemple, sélectionnez ce mode pour que les clients puissent utiliser BranchCache. énumération
topic_type:
- apiref
api_name:
- DownloadMode
api_location:
- deliveryoptimization.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 9ea753ef47dc2e6655d7e707466d7b0448bee7bec1f090b1baf4de04799283d1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118543723"
---
# <a name="downloadmode-enumeration"></a>Énumération DownloadMode

Définit les différents modes de téléchargement utilisés par l’optimisation de la distribution.

## <a name="syntax"></a>Syntaxe


```C++
typedef enum _DownloadMode { 
  DownloadMode_CdnOnly   = 0,
  DownloadMode_Lan       = 1,
  DownloadMode_Group     = 2,
  DownloadMode_Internet  = 3,
  DownloadMode_Simple    = 99,
  DownloadMode_Bypass    = 100
} DownloadMode;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="DownloadMode_CdnOnly"></span><span id="downloadmode_cdnonly"></span><span id="DOWNLOADMODE_CDNONLY"></span>**DownloadMode_CdnOnly**
</dt> <dd>

Ce paramètre désactive la mise en cache d’égal à égal, mais permet toujours l’optimisation de la distribution pour télécharger le contenu à partir des serveurs Microsoft. Ce mode utilise des métadonnées supplémentaires fournies par les services Cloud d’optimisation de la livraison pour une expérience de téléchargement fiable et efficace Peerless.

</dd> <dt>

<span id="DownloadMode_Lan"></span><span id="downloadmode_lan"></span><span id="DOWNLOADMODE_LAN"></span>**DownloadMode_Lan**
</dt> <dd>

Ce mode de fonctionnement par défaut permet le partage entre des pairs d’un même réseau.

</dd> <dt>

<span id="DownloadMode_Group"></span><span id="downloadmode_group"></span><span id="DOWNLOADMODE_GROUP"></span>**DownloadMode_Group**
</dt> <dd>

lorsque le mode groupe est défini, le groupe est automatiquement sélectionné en fonction du site s Active Directory Domain Services (AD DS) du périphérique (Windows 10, version 1607) ou du domaine auquel l’appareil est authentifié (Windows 10, version 1511). En mode Groupe, le peering est effectué sur des sous-réseaux internes, entre les appareils qui appartiennent au même groupe. Cela inclut les appareils situés dans des bureaux distants. Vous pouvez utiliser l’option GroupID pour créer votre propre groupe personnalisé, indépendamment des domaines et des sites AD DS. Le mode de téléchargement groupé est l’option recommandée pour la plupart des organisations qui recherchent la meilleure optimisation de la bande passante avec l’Optimisation de la distribution.

</dd> <dt>

<span id="DownloadMode_Internet"></span><span id="downloadmode_internet"></span><span id="DOWNLOADMODE_INTERNET"></span>**DownloadMode_Internet**
</dt> <dd>

Active les sources homologues Internet pour l’optimisation de la distribution.

</dd> <dt>

<span id="DownloadMode_Simple"></span><span id="downloadmode_simple"></span><span id="DOWNLOADMODE_SIMPLE"></span>**DownloadMode_Simple**
</dt> <dd>

Le mode Simple désactive entièrement les services cloud de la fonction d’optimisation de la distribution (dans le cas des environnements hors ligne). L’optimisation de la distribution bascule automatiquement vers ce mode lorsque les services Cloud d’optimisation de la distribution ne sont pas disponibles, sont inaccessibles ou lorsque la taille du fichier de contenu est inférieure à 10 Mo. Dans ce mode, l’optimisation de la distribution fournit une expérience de téléchargement fiable, sans mise en cache d’égal à égal.

</dd> <dt>

<span id="DownloadMode_Bypass"></span><span id="downloadmode_bypass"></span><span id="DOWNLOADMODE_BYPASS"></span>**DownloadMode_Bypass**
</dt> <dd>

Permet de contourner l’optimisation de la distribution et d’utiliser la fonction BITS, à la place. Par exemple, sélectionnez ce mode pour que les clients puissent utiliser BranchCache.

</dd> </dl>

## <a name="requirements"></a>Configuration requise

| Condition requise | Valeur |
|-------------------------------|----------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 10, les applications de bureau version 1709 \[ uniquement\]<br/>      |
| Serveur minimal pris en charge<br/> | Windows Serveur, version 1709 \[ applications de bureau uniquement\]<br/>  |
| En-tête<br/>                   | <dl> <dt>Deliveryoptimization. h</dt> </dl>               |
