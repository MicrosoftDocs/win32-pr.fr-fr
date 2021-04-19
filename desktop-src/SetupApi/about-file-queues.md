---
description: Une file d’attente de fichiers est une liste d’opérations de fichiers qui sont traitées en même temps. Les opérations de fichier dans la file d’attente peuvent être des opérations de copie, de renommage ou de suppression. La file d’attente de fichiers organise les opérations de fichier par type, en créant des sous-files d’attente de copie, de renommage et de suppression.
ms.assetid: 9ad42c37-1d6b-4f1b-8173-629e2d3678f2
title: À propos des files d’attente de fichiers
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af441a1195bad5116306ca93cfbe658be5b3efc6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106513997"
---
# <a name="about-file-queues"></a>À propos des files d’attente de fichiers

Une file d’attente de fichiers est une liste d’opérations de fichiers qui sont traitées en même temps. Les opérations de fichier dans la file d’attente peuvent être des opérations de copie, de renommage ou de suppression. La file d’attente de fichiers organise les opérations de fichier par type, en créant des sous-files d’attente de copie, de renommage et de suppression.

Ces opérations peuvent être envoyées à la file d’attente dans n’importe quel ordre, et le processus de mise en file d’attente n’a pas besoin d’être contigu. Lorsque la file d’attente est validée, la fonction [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) effectue des opérations sur les fichiers dans l’ordre du type d’opération.

En règle générale, toutes les opérations de fichiers nécessaires pour une installation complète sont mises en file d’attente dans la file d’attente de fichiers, puis traitées dans un lot unique lorsque la file d’attente est validée.

L’un des avantages de la mise en file d’attente des opérations de fichiers sur l’installation de fichiers à partir d’un fichier INF est que vous pouvez simplifier le processus d’installation. Au lieu d’avoir à obtenir des informations de l’utilisateur pour chaque section à installer, vous pouvez obtenir des informations d’installation auprès de l’utilisateur pour tous les fichiers à installer lors de la création de la file d’attente. Cela permet à l’utilisateur d’effectuer d’autres activités, tandis que les opérations de copie gourmandes en temps sont traitées par la fonction [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) .

Un autre avantage des files d’attente de fichiers est que vous pouvez suivre la progression de l’installation dans son ensemble. Lors de l’installation de la section par section à partir d’un fichier INF, les indicateurs de progression tels que les barres de progression peuvent suivre uniquement la section INF actuelle. Lorsque la section suivante est installée, la barre de progression recommence. Avec une file d’attente, le nombre total de fichiers à traiter pendant toute l’installation est connu avant la validation de la file d’attente, et par conséquent, une barre de progression peut être générée pour effectuer le suivi de l’ensemble de l’installation.

Pour plus d'informations, voir les rubriques suivantes :

-   [Ordre de validation des files d’attente](order-of-queue-commitment.md)
-   [Notifications de file d’attente](queue-notifications.md)

 

 



