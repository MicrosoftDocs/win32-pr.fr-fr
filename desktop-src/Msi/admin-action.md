---
description: L’action d’administration est une action de niveau supérieur qui permet d’effectuer des installations administratives.
ms.assetid: 9925a645-5909-42c7-9de8-f908a5e42be9
title: Action d’administration
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 785bd69a8de7da1df9a812f7e89d589b6e939b3eedd6b3cecb66bf86407636cc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119145932"
---
# <a name="admin-action"></a>Action d’administration

L’action d’administration est une action de niveau supérieur qui permet d’effectuer des [installations administratives](administrative-installation.md).

## <a name="sequence-restrictions"></a>Restrictions de séquence

Il n’existe aucune restriction de séquence.

## <a name="actiondata-messages"></a>Messages ActionData

Il n’y a aucun message ActionData.

## <a name="remarks"></a>Remarques

l’action d’administration n’est pas appelée à partir de la séquence de la table d’action, Windows Installer exécute cette action lorsque [**MsiInstallProduct**](/windows/desktop/api/Msi/nf-msi-msiinstallproducta) est appelé avec le paramètre *szCommandLine* défini sur « action = ADMIN » ou l’exécutable de ligne de commande Msiexec.exe est appelé avec le commutateur de ligne de commande « /a ».

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Table AdminUISequence](adminuisequence-table.md)
</dt> <dt>

[Table AdminExecuteSequence](adminexecutesequence-table.md)
</dt> </dl>

 

 



