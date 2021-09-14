---
description: si cette stratégie système par ordinateur est définie sur une valeur supérieure à 0, Windows Installer enregistre les anciennes versions des fichiers dans un cache lorsqu’un correctif est appliqué à une application.
ms.assetid: 986cd521-6907-420d-a2e9-5e0da0069834
title: MaxPatchCacheSize
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8d9930f4a52d3ea0126a19d4dfadae359321f56
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127021353"
---
# <a name="maxpatchcachesize"></a>MaxPatchCacheSize

si cette [stratégie système](system-policy.md) par ordinateur est définie sur une valeur supérieure à 0, Windows Installer enregistre les anciennes versions des fichiers dans un cache lorsqu’un correctif est appliqué à une application. La mise en cache peut augmenter les performances des installations futures qui, sinon, doivent obtenir les anciens fichiers à partir d’une source d’application d’origine.

La valeur de la stratégie MaxPatchCacheSize est le pourcentage maximal d’espace disque que le programme d’installation peut utiliser pour le cache des anciens fichiers. Par exemple, la valeur 20 ne spécifie pas plus de 20% d’utilisation. Si la taille totale du cache atteint le pourcentage d’espace disque spécifié, aucun fichier supplémentaire n’est enregistré dans le cache. La stratégie n’affecte pas les fichiers qui ont déjà été enregistrés.

Si la valeur de la stratégie MaxPatchCacheSize est définie sur 0, aucun fichier supplémentaire n’est enregistré.

Si la stratégie MaxPatchCacheSize n’est pas définie, la valeur par défaut est 10 et un maximum de 10% de l’espace disque peut être utilisé pour enregistrer les anciens fichiers.

## <a name="registry-key"></a>Clé de Registre

**HKEY \_ \_** \\ **stratégies logicielles** de l’ordinateur LOCAL \\  \\ **Microsoft** \\ **Windows** \\ **Installer**

## <a name="data-type"></a>Type de données

**\_valeur DWORD reg**

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[non pris en charge dans Windows Installer 2,0 et versions antérieures](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 



