---
title: Contrôle de compte d’utilisateur et BITS
description: Lorsqu’un utilisateur administrateur ouvre une session sur l’ordinateur, deux jetons d’accès sont créés. L’un est un jeton d’accès utilisateur standard filtré et l’autre est un jeton d’accès administrateur complet.
ms.assetid: 02439ab3-b885-4a2f-b507-0c48d2b30b76
ms.topic: article
ms.date: 7/12/2019
ms.openlocfilehash: 1893c9abc9d783cea6b8ff17e5bcbef47cfc613890c97b45530257950659887d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120004679"
---
# <a name="bits-security-tokens-and-administrator-accounts"></a>Sécurité BITS, jetons et comptes d’administrateur

## <a name="http-server-certificate-callbacks"></a>Rappels de certificat de serveur HTTP
La validation correcte des certificats de serveur est un élément essentiel de la gestion de la sécurité HTTPs. BITS permet de toujours valider les certificats de serveur par rapport à une liste de spécifications spécifiée par [**SetSecurityFlags**](/windows/desktop/api/bits2_5/nf-bits2_5-ibackgroundcopyjobhttpoptions-setsecurityflags). Par défaut, BITS utilise la validation du certificat de style « Browser ».

Vous pouvez également spécifier une fonction personnalisée à appeler afin de valider davantage le certificat. Définissez le rappel de certificat de serveur à l’aide de la méthode [**SetServerCertificateValidationInterface**](/windows/desktop/api/Bits10_3/nf-bits10_3-ibackgroundcopyjobhttpoptions3-setservercertificatevalidationinterface) . Votre méthode est appelée uniquement une fois que le système d’exploitation a validé le certificat sur la base de l’appel [ **SetSecurityFlag** s](/windows/desktop/api/bits2_5/nf-bits2_5-ibackgroundcopyjobhttpoptions-setsecurityflags) . 

## <a name="http-client-certificates"></a>Certificats clients HTTP
Vous pouvez définir un certificat client sur un travail HTTP avec deux méthodes de paramètres de certificat différentes. Vous pouvez définir un certificat par [ID](/windows/desktop/api/bits2_5/nf-bits2_5-ibackgroundcopyjobhttpoptions-setclientcertificatebyid) ou par le nom d' [objet](/windows/desktop/api/bits2_5/nf-bits2_5-ibackgroundcopyjobhttpoptions-setclientcertificatebyname)du certificat. Le certificat client est utilisé lors de la négociation TLS (ou de la renégociation) si le serveur requiert l’authentification du client.

## <a name="write-only-http-headers"></a>En-têtes HTTP en écriture seule
BITS vous aide à protéger les jetons d’authentification HTTP contre les accès indésirables. Souvent, un serveur HTTP nécessite un type de jeton de sécurité ou de chaîne lors du téléchargement ou du chargement d’un fichier sur les serveurs HTTP.

BITS protège ces jetons d’authentification de plusieurs façons.
* BITS vous permet d’utiliser des connexions HTTP protégées par TLS et SSL en spécifiant une URL HTTPs.
* Les en-têtes personnalisés sont toujours conservés dans un format chiffré sur le disque.
* Vous pouvez empêcher que les en-têtes des clients soient renvoyés à d’autres programmes avec la méthode [**IBackgroundCopyJobHttpOptions3 :: MakeCustomHeadersWriteOnly**](/windows/win32/api/Bits10_3/nf-bits10_3-ibackgroundcopyjobhttpoptions3-makecustomheaderswriteonly) .


## <a name="standard-and-administrator-users"></a>Utilisateurs standard et administrateurs
Un utilisateur qui se trouve dans le groupe administrateurs peut exécuter un processus avec un accès utilisateur standard ou dans un état élevé (avec des privilèges d’administrateur). Le service BITS exécute le travail dans l’un ou l’autre des États tant que l’utilisateur a ouvert une session sur l’ordinateur. Toutefois, si l’utilisateur a créé le travail ou a pris possession du travail dans un état élevé, l’utilisateur doit se trouver dans l’état élevé pour récupérer ou modifier le travail (sinon, l’appel échoue avec l’accès refusé (0x80070005)). Pour déterminer l’état élevé d’un travail, appelez la méthode [**IBackgroundCopyJob4 :: GetOwnerElevationState**](/windows/desktop/api/Bits3_0/nf-bits3_0-ibackgroundcopyjob4-getownerelevationstate) .

Un utilisateur standard ne peut pas énumérer ou modifier des travaux appartenant à d’autres utilisateurs.

## <a name="integrity-level"></a>Niveau d’intégrité
En plus de l’état élevé, le niveau d’intégrité du jeton peut déterminer si l’utilisateur peut modifier un travail. Un client ne peut pas modifier les travaux créés par un jeton avec un niveau d’intégrité supérieur. En particulier, de nombreux jetons de système local ont un niveau d’intégrité supérieur au niveau d’intégrité d’une fenêtre avec élévation de privilèges, et ne peuvent donc pas être modifiés par un administrateur à partir d’une fenêtre de commande avec élévation de privilèges ordinaire. par exemple, les Windows Update et les tâches SMS s’exécutent en tant que LocalSystem qui a un niveau d’intégrité supérieur à celui d’un jeton élevé, de sorte qu’un administrateur ne peut pas modifier ou supprimer ces travaux. Pour modifier ce travail, créez une tâche Planificateur de tâches qui s’exécute en tant que système local. La tâche peut exécuter une application console qui utilise l’API BITS, ou la tâche peut exécuter un script qui appelle BitsAdmin.exe. Pour déterminer le niveau d’intégrité utilisé, appelez la méthode [**IBackgroundCopyJob4 :: GetOwnerIntegrityLevel**](/windows/desktop/api/Bits3_0/nf-bits3_0-ibackgroundcopyjob4-getownerintegritylevel) .

## <a name="service-identity"></a>Identité du service
à partir de la Mise à jour de mai 2019 de Windows 10 (10,0 ; Build 18362), les travaux BITS démarrés à partir d’un service conserveront l’identité de service. Cela permet aux services qui souhaitent utiliser BITS de télécharger des fichiers vers ou de télécharger des fichiers à partir d’un répertoire dont les autorisations sont liées au SID de service. En outre, le trafic réseau est correctement attribué au service qui a demandé le travail BITS au lieu d’être attribué à BITS.

 




