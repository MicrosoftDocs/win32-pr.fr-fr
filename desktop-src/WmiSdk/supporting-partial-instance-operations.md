---
description: Un fournisseur n’est pas requis pour prendre en charge les opérations d’instance partielle. Toutefois, un fournisseur doit prendre en charge toutes les sémantiques d’une opération d’instance partielle, traiter une instance complète ou retourner un \_ \_ paramètre non pris en charge par WBEM \_ .
ms.assetid: bc498655-ad6d-44f5-912d-9b7ee95825ec
ms.tgt_platform: multiple
title: Prise en charge des opérations de Partial-Instance
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a2043c09ca129acab6976cabda2b854be464d26036cb5b9df1bc5b82989ccc4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117922849"
---
# <a name="supporting-partial-instance-operations"></a>Prise en charge des opérations de Partial-Instance

Un fournisseur n’est pas requis pour prendre en charge les opérations d’instance partielle. Toutefois, un fournisseur doit prendre en charge toutes les sémantiques d’une opération d’instance partielle, traiter une instance complète ou retourner **un \_ \_ \_ paramètre non pris en charge par WBEM**.

Lorsque vous créez un fournisseur qui prend en charge les opérations d’instance partielle, vous devez respecter les règles suivantes :

-   Réutilisez le même objet de contexte que WMI pour envoyer au fournisseur. WMI utilise la \_ \_ \_ valeur nommée « obtenir ext \_ client \_ Request » pour éviter les interblocages et supprime ce client avant de transférer l’objet de contexte à un fournisseur.
-   Pour les rappels réentrants dans WMI qui ne nécessitent pas d’opération d’instance partielle, assurez-vous de renvoyer le même objet de contexte sans aucune modification. WMI reçoit l’objet de contexte sans la \_ \_ \_ valeur nommée « obtenir ext \_ client \_ Request » définie et supprime toutes les valeurs nommées associées à des opérations d’instance partielle de l’objet de contexte avant de le passer à d’autres fournisseurs. Le fait de ne pas modifier l’objet de contexte empêche les autres fournisseurs de recevoir des opérations de récupération d’instance partielle destinées à un objet différent et non lié.
-   Pour effectuer une opération d’instance partielle réentrante pendant l’exécution d’une requête, définissez la \_ \_ \_ valeur nommée « obtenir ext \_ client Request » manquante et la \_ propriété Clear. Si vous le souhaitez, vous pouvez modifier les propriétés de la \_ \_ \_ valeur nommée « récupérer \_ les propriétés ext » avant de renvoyer l’objet de contexte dans WMI avec l’appel réentrant.
-   N’accédez pas à l’objet de contexte après l’avoir retourné à WMI lors d’un appel réentrant ; d’autres fournisseurs peuvent modifier les listes de propriétés ou d’autres valeurs pendant la réentrance. Vous pouvez examiner ou modifier l’objet de contexte uniquement pendant la durée de l’appel [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) que vous implémentez.

 

 



