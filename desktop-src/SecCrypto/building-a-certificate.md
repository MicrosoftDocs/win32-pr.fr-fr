---
description: Explique les appels requis pour générer un certificat.
ms.assetid: 74154b3b-75fc-412f-835c-1a6f54e688c6
title: Génération d’un certificat
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8f237fd729499aa5153f12f68657e2ce227da7b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868798"
---
# <a name="building-a-certificate"></a>Génération d’un certificat

L’ordre des appels dans la génération d’un certificat est le suivant :

1.  L' [*autorité de certification*](../secgloss/c-gly.md) initialise les modules par le biais d’appels à [**ICertPolicy**](/windows/desktop/api/Certpol/nn-certpol-icertpolicy) et [**ICertExit**](/windows/desktop/api/Certexit/nn-certexit-icertexit) (se produit une fois lors de l’initialisation du serveur). L’autorité de certification initialise les modules de stratégie et de sortie en appelant [**ICertPolicy2 :: Initialize**](/windows/desktop/api/Certpol/nf-certpol-icertpolicy-initialize) et [**ICertExit :: Initialize**](/windows/desktop/api/Certexit/nf-certexit-icertexit-initialize).
2.  Un intermédiaire appelle l’autorité de certification via [**ICertConfig**](/windows/desktop/api/Certcli/nn-certcli-icertconfig) (se produit une fois par initialisation intermédiaire). L’intermédiaire trouve la chaîne de configuration nécessaire en appelant [**ICertConfig :: GetConfig**](/windows/desktop/api/Certcli/nf-certcli-icertconfig-getconfig).
3.  Le client appelle l’intermédiaire via une interface spécifique à l’intermédiaire (se produit une fois par demande). Le client envoie une [*demande de certificat*](../secgloss/c-gly.md) à l’intermédiaire. Il peut s’agir, par exemple, de Microsoft Internet Explorer qui envoie une demande par le biais du [contrôle d’inscription de certificats](certificate-enrollment-control.md) à Microsoft Internet Information Services.
4.  Intermédiaire vers CA via [**ICertRequest**](/windows/desktop/api/Certcli/nn-certcli-icertrequest) (se produit une fois par demande). L’intermédiaire envoie la demande de certificat à l’autorité de certification via [**ICertRequest :: Submit**](/windows/desktop/api/Certcli/nf-certcli-icertrequest-submit). Dans le cas de Internet Information Services, cela peut être effectué par le biais de scripts Active Server pages.
5.  L’autorité de certification appelle le module de stratégie par le biais de l’interface [**ICertPolicy**](/windows/desktop/api/Certpol/nn-certpol-icertpolicy) (se produit une fois par demande). L’autorité de certification informe le module de stratégie qu’une demande est arrivée en appelant [**ICertPolicy :: VerifyRequest**](/windows/desktop/api/Certpol/nf-certpol-icertpolicy-verifyrequest). Le module de stratégie peut examiner la demande et modifier le certificat en appelant les méthodes de l’interface [**ICertServerPolicy**](/windows/desktop/api/Certif/nn-certif-icertserverpolicy) . Le module de stratégie peut alors indiquer que la demande est correcte (dans ce cas, le certificat est généré à ce stade), que la demande doit être refusée ou que la demande doit être suspendue.
6.  Facultatif L’administrateur appelle l’autorité de certification par le biais de l’interface [**ICertAdmin**](/windows/desktop/api/Certadm/nn-certadm-icertadmin) . Si la demande est suspendue, l’administrateur peut renvoyer ou refuser la demande, ou modifier les attributs et les extensions de demande. Notez que si la demande est renvoyée, le module de stratégie aura une autre possibilité de traiter la demande (à la suite d’un appel à [**ICertPolicy :: VerifyRequest**](/windows/desktop/api/Certpol/nf-certpol-icertpolicy-verifyrequest)). La tâche consistant à renvoyer ou refuser la demande peut être effectuée au moyen du composant logiciel enfichable MMC de l’autorité de certification ou d’une autre application qui utilise **ICertAdmin**.
7.  L’autorité de certification appelle le module de sortie par le biais de l’interface [**ICertExit**](/windows/desktop/api/Certexit/nn-certexit-icertexit) . Si le module de sortie a indiqué (quand [**ICertExit :: Initialize**](/windows/desktop/api/Certexit/nf-certexit-icertexit-initialize) a été appelé, à l’étape 1) qu’il souhaite voir les certificats émis ou les demandes maintenues en attente, l’autorité de certification appellera [**ICertExit :: Notify**](/windows/desktop/api/Certexit/nf-certexit-icertexit-notify).
8.  Le module de sortie appelle l’autorité de certification par le biais de l’interface [**ICertServerExit**](/windows/desktop/api/Certif/nn-certif-icertserverexit) . Le module de sortie peut examiner la demande et le nouveau certificat en appelant les méthodes de **ICertServerExit**.

 

 
