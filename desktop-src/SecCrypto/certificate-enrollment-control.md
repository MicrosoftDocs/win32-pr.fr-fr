---
description: Le contrôle d’inscription de certificat peut être utilisé par une application qui doit demander qu’un certificat soit émis pour un objet nommé.
ms.assetid: ce6661b0-7ed2-452f-a54c-6705d14f3298
title: Contrôle d’inscription de certificat
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e417a9db7984cbb58b7c2e3b51d828b6d61a97b6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127416493"
---
# <a name="certificate-enrollment-control"></a>Contrôle d’inscription de certificat

Le contrôle d’inscription de certificat peut être utilisé par une application qui doit demander qu’un certificat soit émis pour un objet nommé. Il est conçu pour accepter des données sous la forme d’une chaîne binaire (BSTR). les données peuvent provenir d’une page web ou de l’interface utilisateur du système de développement Visual Basic ou Visual C++. La sortie du contrôle d’inscription de certificats est une demande de \# certificat PKCS 10 qui peut être envoyée à une [*autorité de certification*](../secgloss/c-gly.md) .

![contrôle d’inscription de certificat](images/xen-arch.png)

Les informations nécessaires sur l’utilisateur, l’objet du certificat, sont collectées par l’interface utilisateur. Ces informations sont fournies sous la forme d’une entrée BSTR dans le contrôle d’inscription de certificat. Le contrôle d’inscription de certificat génère la clé de signature, la clé d’échange de clés ou les deux paires de clés appropriées. Le contrôle génère et signe ensuite une \# demande de [*certificat*](../secgloss/c-gly.md) PKCS 10 à l’aide de la [*clé privée*](../secgloss/p-gly.md)générée. Le contrôle d’inscription de certificat lie ensuite la paire de clés à un certificat factice temporaire qui est stocké dans le magasin de demandes jusqu’à ce que le certificat émis soit retourné par une autorité de certification. Enfin, l’application envoie la \# demande de certificat PKCS 10 à une autorité de certification.

Si l’autorité de certification approuve la demande de certificat, l’autorité de certification crée un certificat contenant la clé publique. L’autorité de certification signe et retourne également le certificat.

Lorsque le certificat demandé est retourné par l’autorité de certification, l’application transmet le \# message PKCS 7 au contrôle d’inscription de certificat où le certificat ou la chaîne de certificats est extrait du \# message PKCS 7. Le certificat et tous les autres certificats de la chaîne d’approbation sont stockés dans un [*magasin de certificats*](../secgloss/c-gly.md). Le certificat retourné n’est pas modifié de quelque manière que ce soit. Toute application prenant en charge les certificats peut maintenant accéder à ce certificat à partir du magasin.

Le contrôle d’inscription de carte à puce est utilisé par un administrateur pour s’inscrire au nom des utilisateurs de carte à puce. Le processus d’inscription entraîne l’émission d’un certificat stocké sur la carte à puce d’un utilisateur.

Le contrôle d’inscription de carte à puce est contenu dans Scrdenrl.dll et se compose d’un objet, **SCrdEnr**. Aucun autre objet n’est inclus dans Scrdenrl.dll. cet objet d’inscription de carte à puce peut être utilisé avec un langage de script, tel que Visual Basic scripting Edition (VBScript).

Un [*lecteur de carte à puce*](../secgloss/r-gly.md) doit être installé sur l’ordinateur exécutant le contrôle d’inscription de carte à puce.

En outre, l’émetteur de carte à puce doit avoir obtenu un certificat de signature basé sur le modèle de certificat « EnrollmentAgent ». Ce certificat de signature sera utilisé pour signer la demande de certificat générée pour le compte du destinataire de la carte à puce. Par défaut, les administrateurs de domaine sont autorisés à demander un certificat basé sur le modèle « agent d’inscription ». Un autre utilisateur peut être autorisé à s’inscrire pour obtenir un certificat « EnrollmentAgent » (au moyen du composant logiciel enfichable MMC sites et services Active Directory). Toutefois, cela permet à cet utilisateur d’auto-émettre une carte à puce avec des privilèges d’administrateur de domaine.

 

 
