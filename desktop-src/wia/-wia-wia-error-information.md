---
description: les api d’Acquisition d’images Windows (WIA) renvoient leur état d’achèvement dans une valeur de retour HRESULT.
ms.assetid: 4f3b4292-7aad-4a0a-9cd7-ef8438e57ab3
title: Informations sur l’erreur WIA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce8181cb4d3f578fa9322ecaa81d588423bb403be3b38a76c2dbac17a19fe010
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120056959"
---
# <a name="wia-error-information"></a>Informations sur l’erreur WIA

les api d’Acquisition d’images Windows (WIA) renvoient leur état d’achèvement dans une valeur de retour HRESULT. Les applications vérifient ces valeurs de retour par rapport à la constante d’installation \_ WIA pour déterminer si l’erreur nécessite une intervention de l’utilisateur, telle qu’un bourrage papier, et les signaler à l’utilisateur. En outre, toutes les erreurs au niveau du pilote sont consignées en détail dans le journal des événements, à l’aide des chaînes d’erreur fournies par le minipilote d’appareil. Pour obtenir la liste des codes d’erreur spécifiques à WIA, consultez [codes d’erreur](-wia-error-codes.md).

 

 



