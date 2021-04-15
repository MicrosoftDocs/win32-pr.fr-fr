---
description: Si le compilateur MOF ne peut pas terminer la compilation d’un fichier MOF, l’espace de stockage WMI peut être laissé dans un État indéfini.
ms.assetid: 13adc666-6588-4cfd-a5eb-17da93434468
ms.tgt_platform: multiple
title: Gestion des erreurs avec le compilateur MOF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 905b406020787de894a2821b501ee465ab63ea5e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104485817"
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

 

 



