---
title: Retour d’informations sur l’erreur
description: Retour d’informations sur l’erreur
ms.assetid: 4206f2e5-db01-458c-93cb-10c5cd4a4536
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 545c697be7da64362ecce0f5b4c45272832ad682d8b4dd0eb5234620b993e5f3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118309641"
---
# <a name="returning-error-information"></a>Retour d’informations sur l’erreur

À l’aide des interfaces et des fonctions de gestion des erreurs COM, vous pouvez retourner des informations sur les erreurs en effectuant les étapes suivantes :

1.  Implémentez l’interface [**ISupportErrorInfo**](/windows/win32/api/oaidl/nn-oaidl-isupporterrorinfo) .
2.  Pour créer une instance de l’objet d’erreur générique, appelez la fonction [**CreateErrorInfo**](/windows/win32/api/oleauto/nf-oleauto-createerrorinfo) .
3.  Pour définir son contenu, utilisez les méthodes [**ICreateErrorInfo**](/windows/win32/api/oaidl/nn-oaidl-icreateerrorinfo) .
4.  Pour associer l’objet d’erreur au thread logique actuel, appelez la fonction [**SetErrorInfo**](/windows/win32/api/oleauto/nf-oleauto-seterrorinfo) .

Les interfaces de gestion des erreurs créent et gèrent un objet d’erreur qui fournit des informations sur l’erreur. L’objet d’erreur n’est pas le même que l’objet qui a rencontré l’erreur. Il s’agit d’un objet distinct associé au thread d’exécution actuel.

 

 