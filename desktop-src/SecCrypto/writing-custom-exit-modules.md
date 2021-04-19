---
description: Les modules de sortie personnalisés doivent implémenter l’interface ICertExit, qui est appelée par le moteur serveur.
ms.assetid: 509e7945-b656-4c4c-b5eb-45fbe80377c7
title: Écriture de modules de sortie personnalisés
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81798996059e878ef11dbcdf290298094d0849cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106541228"
---
# <a name="writing-custom-exit-modules"></a>Écriture de modules de sortie personnalisés

Les modules de sortie personnalisés doivent implémenter l’interface [**ICertExit**](/windows/desktop/api/Certexit/nn-certexit-icertexit) , qui est appelée par le moteur serveur. La méthode [**ICertExit :: Initialize**](/windows/desktop/api/Certexit/nf-certexit-icertexit-initialize) est appelée par le moteur serveur lorsque le module de sortie est chargé. Elle permet au module de sortie d’effectuer l’initialisation et retourne une valeur qui informe le moteur serveur des types d’événements pour lesquels il souhaite recevoir la notification. La méthode [**ICertExit :: GetDescription**](/windows/desktop/api/Certexit/nf-certexit-icertexit-getdescription) doit retourner une chaîne de description lorsque le moteur du serveur le demande. La méthode [**ICertExit :: Notify**](/windows/desktop/api/Certexit/nf-certexit-icertexit-notify) est appelée par le moteur du serveur pour informer le module de sortie qu’un événement s’est produit.

Les modules de sortie peuvent appeler l’interface [**ICertServerExit**](/windows/desktop/api/Certif/nn-certif-icertserverexit) , qui prend en charge la plupart des méthodes de l’interface [**ICertServerPolicy**](/windows/desktop/api/Certif/nn-certif-icertserverpolicy) , à l’exception des méthodes [**SetCertificateExtension**](/windows/desktop/api/Certif/nf-certif-icertserverpolicy-setcertificateextension) et [**SetCertificateProperty**](/windows/desktop/api/Certif/nf-certif-icertserverpolicy-setcertificateproperty) .

Pour plus d’informations sur la suppression du module de sortie existant et l’installation d’un nouveau, consultez la rubrique relative à la personnalisation du module de sortie dans l’aide de.

 

 



