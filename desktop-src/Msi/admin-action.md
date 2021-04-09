---
description: L’action d’administration est une action de niveau supérieur qui permet d’effectuer des installations administratives.
ms.assetid: 9925a645-5909-42c7-9de8-f908a5e42be9
title: Action d’administration
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00106c9ab7877918e122f1ec9bd201fe30bb68b1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864509"
---
# <a name="admin-action"></a>Action d’administration

L’action d’administration est une action de niveau supérieur qui permet d’effectuer des [installations administratives](administrative-installation.md).

## <a name="sequence-restrictions"></a>Restrictions de séquence

Il n’existe aucune restriction de séquence.

## <a name="actiondata-messages"></a>Messages ActionData

Il n’y a aucun message ActionData.

## <a name="remarks"></a>Notes

L’action d’administration n’est pas appelée à partir de la séquence de la table d’action, Windows Installer exécute cette action lorsque [**MsiInstallProduct**](/windows/desktop/api/Msi/nf-msi-msiinstallproducta) est appelé avec le paramètre *szCommandLine* défini sur « action = admin » ou l’exécutable de ligne de commande Msiexec.exe est appelé avec le commutateur de ligne de commande « /a ».

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Table AdminUISequence](adminuisequence-table.md)
</dt> <dt>

[Table AdminExecuteSequence](adminexecutesequence-table.md)
</dt> </dl>

 

 



