---
description: Un fournisseur WMI à hautes performances augmente considérablement la vitesse à laquelle un client WMI peut obtenir des informations à partir d’un fournisseur d’instances WMI.
ms.assetid: 767a16bb-44b6-4c56-b79b-23241fcc216e
ms.tgt_platform: multiple
title: Amélioration de l’efficacité d’un fournisseur d’instances
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0fecd0d8a20a3dcccd2878996823a7eb8a7ec0f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866885"
---
# <a name="improving-the-efficiency-of-an-instance-provider"></a>Amélioration de l’efficacité d’un fournisseur d’instances

Un fournisseur WMI à hautes performances augmente considérablement la vitesse à laquelle un client WMI peut obtenir des informations à partir d’un fournisseur d’instances WMI. La principale modification est qu’un fournisseur à hautes performances s’exécute en tant que serveur in-process pour l’application cliente ou WMI. En plaçant le fournisseur dans le processus client, vous pouvez accélérer l’interaction entre les deux.

Pour plus d’informations sur la façon de faire de votre fournisseur d’instances un fournisseur à hautes performances, consultez [création d’un fournisseur d’instances dans un fournisseur de High-Performance](making-an-instance-provider-into-a-high-performance-provider.md).

 

 



