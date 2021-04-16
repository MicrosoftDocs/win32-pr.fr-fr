---
description: Si cette stratégie système par ordinateur est définie sur une valeur supérieure à 0, Windows Installer enregistre les anciennes versions des fichiers dans un cache lorsqu’un correctif est appliqué à une application.
ms.assetid: 986cd521-6907-420d-a2e9-5e0da0069834
title: MaxPatchCacheSize
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8d9930f4a52d3ea0126a19d4dfadae359321f56
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104485264"
---
# <a name="maxpatchcachesize"></a>MaxPatchCacheSize

Si cette [stratégie système](system-policy.md) par ordinateur est définie sur une valeur supérieure à 0, Windows Installer enregistre les anciennes versions des fichiers dans un cache lorsqu’un correctif est appliqué à une application. La mise en cache peut augmenter les performances des installations futures qui, sinon, doivent obtenir les anciens fichiers à partir d’une source d’application d’origine.

La valeur de la stratégie MaxPatchCacheSize est le pourcentage maximal d’espace disque que le programme d’installation peut utiliser pour le cache des anciens fichiers. Par exemple, la valeur 20 ne spécifie pas plus de 20% d’utilisation. Si la taille totale du cache atteint le pourcentage d’espace disque spécifié, aucun fichier supplémentaire n’est enregistré dans le cache. La stratégie n’affecte pas les fichiers qui ont déjà été enregistrés.

Si la valeur de la stratégie MaxPatchCacheSize est définie sur 0, aucun fichier supplémentaire n’est enregistré.

Si la stratégie MaxPatchCacheSize n’est pas définie, la valeur par défaut est 10 et un maximum de 10% de l’espace disque peut être utilisé pour enregistrer les anciens fichiers.

## <a name="registry-key"></a>Clé de Registre

**HKEY \_ \_** \\ **Stratégies logicielles** de l’ordinateur local \\  \\ **Microsoft** \\ **Windows** \\ **installer**

## <a name="data-type"></a>Type de données

**\_valeur DWORD reg**

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Non pris en charge dans Windows Installer 2,0 et versions antérieures](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 



