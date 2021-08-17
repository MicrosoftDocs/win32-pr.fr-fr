---
description: Si le compilateur MOF ne peut pas terminer la compilation d’un fichier MOF, l’espace de stockage WMI peut être laissé dans un État indéfini.
ms.assetid: 13adc666-6588-4cfd-a5eb-17da93434468
ms.tgt_platform: multiple
title: Gestion des erreurs avec le compilateur MOF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03f5174af836a0b27824c40486364cc81809db97b9608e6b1c813c4c1029d3aa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118993169"
---
# <a name="handling-errors-with-the-mof-compiler"></a>Gestion des erreurs avec le compilateur MOF

Si le compilateur MOF ne peut pas terminer la compilation d’un fichier MOF, l’espace de stockage WMI peut être laissé dans un État indéfini. Par exemple, si vous compilez un fichier MOF et que vous utilisez le commutateur de ligne de commande **-Class : CreateOnly** , la compilation se termine si une classe spécifiée dans le fichier MOF existe déjà. Le compilateur MOF stocke dans le référentiel toutes les classes ou instances qui ont été définies jusqu’au point où le compilateur s’arrête. Dans certains cas, cela peut rendre le référentiel WMI dans une condition non définie.

Dans ce cas, vous devrez peut-être arrêter WMI, supprimer le référentiel WMI et le faire régénérer par WMI. Tous les fichiers MOF contenant la [commande de préprocesseur](preprocessor-commands.md) [**pragma AutoRecover**](pragma-autorecover.md) sont reconstruits lors du redémarrage de WMI. Vous devez recompiler manuellement tous les fichiers MOF qui n’incluent pas d' `#pragma autorecover` instruction.

Pour plus d’informations sur la façon de déclarer des classes et des instances à l’aide de la syntaxe MOF, consultez [conception de classes format MOF (MOF)](designing-managed-object-format--mof--classes.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Compilation des fichiers MOF](compiling-mof-files.md)
</dt> <dt>

[**mofcomp**](mofcomp.md)
</dt> <dt>

[Commandes de préprocesseur](preprocessor-commands.md)
</dt> </dl>

 

 



