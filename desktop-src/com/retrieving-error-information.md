---
title: Extraction des informations sur les erreurs
description: Extraction des informations sur les erreurs
ms.assetid: 51a0e401-43f2-4738-9799-a96e2580a29f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e26844505b7c5de3e39c3199a6087c94f35bed9f64ef11a65d1c6df9a3dd4e9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118309651"
---
# <a name="retrieving-error-information"></a>Extraction des informations sur les erreurs

À l’aide des interfaces et des fonctions de gestion des erreurs COM, vous pouvez récupérer les informations d’erreur comme suit :

1.  Vérifiez si la valeur retournée représente une erreur que l’objet est prêt à gérer.
2.  Appelez [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) pour obtenir un pointeur vers l’interface [**ISupportErrorInfo**](/windows/win32/api/oaidl/nn-oaidl-isupporterrorinfo) . Appelez ensuite [**ISupportErrorInfo :: InterfaceSupportsErrorInfo**](/windows/win32/api/oaidl/nf-oaidl-isupporterrorinfo-interfacesupportserrorinfo) pour vérifier que l’erreur a été déclenchée par l’objet qui l’a retourné et que l’objet d’erreur se rapporte à l’erreur actuelle et non à un appel précédent.
3.  Pour obtenir un pointeur vers l’objet d’erreur, appelez la fonction [**GetErrorInfo**](/windows/win32/api/oleauto/nf-oleauto-geterrorinfo) .
4.  Pour récupérer des informations de l’objet Error, utilisez les méthodes [**IErrorInfo**](/windows/win32/api/oaidl/nn-oaidl-ierrorinfo) .

Si l’objet n’est pas préparé à gérer l’erreur mais doit propager les informations d’erreur plus loin dans la chaîne d’appel, il doit simplement transmettre la valeur de retour à son appelant. Étant donné que la fonction [**GetErrorInfo**](/windows/win32/api/oleauto/nf-oleauto-geterrorinfo) efface les informations d’erreur et transmet la propriété de l’objet d’erreur à l’appelant, la fonction doit être appelée uniquement par l’objet qui gère l’erreur.

 

 