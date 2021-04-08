---
description: L’action de publication est une action de niveau supérieur appelée pour installer ou supprimer des composants publiés.
ms.assetid: d9c843e4-fcd9-4d47-9ca9-ffa83ed80574
title: Action de publication
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0985990d69863f250cfd6f589deb43a59f9c66e9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103756244"
---
# <a name="advertise-action"></a>Action de publication

L’action de publication est une action de niveau supérieur appelée pour installer ou supprimer des composants publiés.

## <a name="sequence-restrictions"></a>Restrictions de séquence

Il n’existe aucune restriction de séquence.

## <a name="actiondata-messages"></a>Messages ActionData

Il n’y a aucun message ActionData.

## <a name="remarks"></a>Notes

La [*publication*](a-gly.md) fait référence à la capacité du programme d’installation à fournir les interfaces de chargement et de lancement d’une application sans installer physiquement l’application. Le programme d’installation n’installe pas les composants nécessaires tant qu’un utilisateur ou une application n’a pas activé une interface publiée. Ce concept est appelé [*Install-on-demand*](i-gly.md).

L’action de publication n’est pas appelée à partir de la séquence de la table d’action, le Windows Installer exécute cette action lorsque l’exécutable de ligne de commande Msiexec.exe est appelé avec le commutateur de ligne de commande'/j’ou lorsque [**MsiInstallProduct**](/windows/desktop/api/Msi/nf-msi-msiinstallproducta) est appelé avec le paramètre *SZCOMMANDLINE* défini sur action = advertise.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Table AdvtExecuteSequence](advtexecutesequence-table.md)
</dt> </dl>

 

 



