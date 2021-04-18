---
description: Les API WIA (Windows Image Acquisition) renvoient leur état d’achèvement dans une valeur de retour HRESULT.
ms.assetid: 4f3b4292-7aad-4a0a-9cd7-ef8438e57ab3
title: Informations sur l’erreur WIA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31bcbba9e42d8b7a95b892eb8bba14a56ad758e3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106516264"
---
# <a name="wia-error-information"></a>Informations sur l’erreur WIA

Les API WIA (Windows Image Acquisition) renvoient leur état d’achèvement dans une valeur de retour HRESULT. Les applications vérifient ces valeurs de retour par rapport à la constante d’installation \_ WIA pour déterminer si l’erreur nécessite une intervention de l’utilisateur, telle qu’un bourrage papier, et les signaler à l’utilisateur. En outre, toutes les erreurs au niveau du pilote sont consignées en détail dans le journal des événements, à l’aide des chaînes d’erreur fournies par le minipilote d’appareil. Pour obtenir la liste des codes d’erreur spécifiques à WIA, consultez [codes d’erreur](-wia-error-codes.md).

 

 



