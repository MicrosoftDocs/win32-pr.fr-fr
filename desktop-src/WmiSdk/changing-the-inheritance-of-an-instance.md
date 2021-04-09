---
description: Vous pouvez trouver une situation dans laquelle une instance qui a été créée en tant qu’enfant d’une classe parente doit modifier les classes parentes et devenir l’enfant d’une autre classe parente.
ms.assetid: 6d0fd456-81ab-4665-bb88-f9fb29fbbd39
ms.tgt_platform: multiple
title: Modification de l’héritage d’une instance
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a35de3dcc37d91b318ab60fb5a520cb4da10e59
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103865677"
---
# <a name="changing-the-inheritance-of-an-instance"></a>Modification de l’héritage d’une instance

Vous pouvez trouver une situation dans laquelle une instance qui a été créée en tant qu’enfant d’une classe parente doit modifier les classes parentes et devenir l’enfant d’une autre classe parente. Par exemple, vous pouvez avoir une classe dérivée, **ManualService**, décrivant un service manuel, et une classe dérivée, **Autoservice**, décrivant un service automatique. Les deux classes ont un grand nombre de propriétés. Toutes les propriétés ne sont pas identiques. Pour passer d’un service manuel à un service automatique, vous devez également remplacer l’instance de **ManualService** qui représente le service par **Autoservice**. Dans la version actuelle de WMI, vous ne pouvez pas appeler la méthode [**IWbemServices ::P utinstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstance) avec le paramètre *Pint* qui pointe vers une instance d' **Autoservice** et les propriétés de clé qui décrivent l’instance **ManualService** . Si vous le faites, vous supprimez implicitement l’instance **ManualService** d’origine. En résumé, une fois que vous avez établi la classe d’une instance, vous pouvez uniquement modifier la classe parente d’une instance en supprimant l’instance et en recréant l’instance en tant qu’instance de la nouvelle classe parente.

La procédure suivante décrit comment déplacer une instance d’une classe vers une autre.

**Pour déplacer une instance d’une classe vers une autre classe**

1.  Supprimez l’instance de la classe d’origine.
2.  Créez l’instance sous la nouvelle classe.

    WMI n’autorise pas les applications à déplacer une instance en la créant dans la nouvelle classe, puis en la mettant à jour avec la clé de l’instance d’origine.

Pour plus d’informations, consultez [manipulation d’informations sur les classes et les instances](manipulating-class-and-instance-information.md).

 

 



