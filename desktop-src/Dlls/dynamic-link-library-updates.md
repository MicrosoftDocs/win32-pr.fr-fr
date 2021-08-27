---
description: Il est parfois nécessaire de remplacer une DLL par une version plus récente.
ms.assetid: 82349a33-dc2c-4309-b0fc-890f230e3f2c
title: Mises à jour de la bibliothèque de Dynamic-Link
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f294e16efac60da843c14d200aaa768d4fc78ce8a922cb0aa6958756a9903be0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120075539"
---
# <a name="dynamic-link-library-updates"></a>Mises à jour de la bibliothèque de Dynamic-Link

Il est parfois nécessaire de remplacer une DLL par une version plus récente. Avant de remplacer une DLL, effectuez une vérification de la version pour vous assurer que vous remplacez une version antérieure par une version plus récente. Il est possible de remplacer une DLL en cours d’utilisation. La méthode que vous utilisez pour remplacer les dll en cours d’utilisation dépend du système d’exploitation que vous utilisez. sur Windows XP et versions ultérieures, les applications doivent utiliser [des applications isolées et des assemblys côte à côte](/windows/desktop/SbsCs/isolated-applications-and-side-by-side-assemblies-portal).

Il n’est pas nécessaire de redémarrer l’ordinateur si vous effectuez les étapes suivantes :

1.  Utilisez la fonction [**MoveFileEx**](/windows/desktop/api/winbase/nf-winbase-movefileexa) pour renommer la dll remplacée. Ne spécifiez pas \_ de copie MOVEFILE autorisée, et assurez-vous que \_ le fichier renommé se trouve sur le même volume que celui qui contient le fichier d’origine. Vous pouvez également simplement renommer le fichier dans le même répertoire en lui attribuant une extension différente.
2.  Copiez la nouvelle DLL dans le répertoire qui contient la DLL renommée. Toutes les applications utiliseront désormais la nouvelle DLL.
3.  Utilisez [**MoveFileEx**](/windows/desktop/api/winbase/nf-winbase-movefileexa) avec \_ le délai MOVEFILE \_ jusqu' \_ au redémarrage pour supprimer la dll renommée.

Avant de procéder à ce remplacement, les applications utiliseront la DLL d’origine jusqu’à ce qu’elle soit déchargée. Une fois le remplacement effectué, les applications utiliseront la nouvelle DLL. Lorsque vous écrivez une DLL, vous devez veiller à ce qu’elle soit préparée pour cette situation, en particulier si la DLL conserve des informations d’État globales ou communique avec d’autres services. Si la DLL n’est pas préparée pour une modification des informations d’État globales ou des protocoles de communication, la mise à jour de la DLL vous oblige à redémarrer l’ordinateur pour s’assurer que toutes les applications utilisent la même version de la DLL.

 

 
