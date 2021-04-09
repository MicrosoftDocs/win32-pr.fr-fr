---
description: Pour récupérer des données du Registre, une application énumère généralement les sous-clés d’une clé jusqu’à ce qu’elle en trouve une spécifique, puis récupère les données à partir de la ou des valeurs associées.
ms.assetid: ce4be388-5506-4d01-a73c-33372ef4ccd7
title: Récupération de données à partir du Registre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45d8dd6f6e4d667cf2760c7cba441200755fb6c3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104035158"
---
# <a name="retrieving-data-from-the-registry"></a>Récupération de données à partir du Registre

Pour récupérer des données du Registre, une application énumère généralement les sous-clés d’une clé jusqu’à ce qu’elle en trouve une spécifique, puis récupère les données à partir de la ou des valeurs associées. Une application peut appeler la fonction [**RegEnumKeyEx**](/windows/desktop/api/Winreg/nf-winreg-regenumkeyexa) pour énumérer les sous-clés d’une clé donnée.

Pour récupérer des données détaillées sur une sous-clé particulière, une application peut appeler la fonction [**RegQueryInfoKey**](/windows/desktop/api/Winreg/nf-winreg-regqueryinfokeya) . La fonction [**RegGetKeySecurity**](/windows/desktop/api/winreg/nf-winreg-reggetkeysecurity) récupère une copie du descripteur de sécurité protégeant une clé.

Une application peut utiliser la fonction [**RegEnumValue**](/windows/desktop/api/Winreg/nf-winreg-regenumvaluea) pour énumérer les valeurs d’une clé donnée et la fonction [**RegQueryValueEx**](/windows/desktop/api/Winreg/nf-winreg-regqueryvalueexa) pour récupérer une valeur particulière pour une clé. Une application appelle généralement **RegEnumValue** pour déterminer les noms de valeur, puis **RegQueryValueEx** pour récupérer les données pour les noms.

La fonction [**RegQueryMultipleValues**](/windows/desktop/api/Winreg/nf-winreg-regquerymultiplevaluesa) récupère le type et les données pour une liste de noms de valeurs associés à une clé de Registre ouverte. Cette fonction est utile pour les fournisseurs de clés dynamiques, car elle garantit la cohérence des données en extrayant plusieurs valeurs dans une opération atomique.

Étant donné que d’autres applications peuvent modifier les données d’une valeur de Registre entre le moment où votre application peut lire une valeur et l’utiliser, vous devrez peut-être vous assurer que votre application contient les données les plus récentes. Vous pouvez utiliser la fonction [**RegNotifyChangeKeyValue**](/windows/desktop/api/Winreg/nf-winreg-regnotifychangekeyvalue) pour notifier le thread appelant lorsqu’il y a des modifications apportées aux attributs ou au contenu d’une clé de Registre, ou si la clé est supprimée. La fonction signale un objet d’événement pour notifier l’appelant. Si le thread qui appelle **RegNotifyChangeKeyValue** se termine, l’événement est signalé et l’analyse de la clé de Registre est arrêtée.

Vous pouvez contrôler ou spécifier les modifications qui doivent être signalées à l’aide d’un filtre ou d’un indicateur Notify. En règle générale, les modifications sont signalées en signalant un événement que vous spécifiez à la fonction. Notez que la fonction [**RegNotifyChangeKeyValue**](/windows/desktop/api/Winreg/nf-winreg-regnotifychangekeyvalue) ne fonctionne pas avec les handles distants.

Pour surveiller les opérations du registre plus en détail, consultez [**Registry**](/windows/desktop/ETW/registry).

 

 
