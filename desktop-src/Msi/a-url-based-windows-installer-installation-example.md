---
description: cet exemple montre comment créer une installation d’un package Windows Installer basée sur une URL.
ms.assetid: a38a1132-43b4-449d-b134-f351ce370223
title: Exemple d’installation de Windows Installer basée sur une URL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57a210eb1b93202930309223b49c737aa85b1812
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127092965"
---
# <a name="a-url-based-windows-installer-installation-example"></a>Exemple d’installation de Windows Installer basée sur une URL

cet exemple montre comment créer une installation d’un package Windows Installer basée sur une URL. pour plus d’informations sur la sécurisation des installations et l’utilisation des certificats numériques, consultez [instructions de création d’installations sécurisées](guidelines-for-authoring-secure-installations.md) et de [Signatures numériques et de Windows Installer](digital-signatures-and-windows-installer.md).

Pour reproduire cet exemple, vous avez besoin de l’utilitaire [SignTool](../seccrypto/signtool.md) . pour plus d’informations, consultez les informations de référence sur les [outils CryptoAPI](../seccrypto/cryptoapi-tools-reference.md) dans le kit de développement logiciel (SDK) de Microsoft Windows. vous avez également besoin des [Msistuff.exe](msistuff-exe.md) et des utilitaires Setup.exe des [composants SDK Windows pour les développeurs Windows Installer](platform-sdk-components-for-windows-installer-developers.md). Pour plus d’informations, consultez [démarrage du téléchargement Internet](internet-download-bootstrapping.md).

L’exemple présente les spécifications suivantes :

-   Lorsque les utilisateurs accèdent à votre site Web et cliquent sur le lien « installation MySetup », ils disposent de la possibilité d’enregistrer ou d’exécuter à partir de cet emplacement. si l’utilisateur choisit d’exécuter à partir de cet emplacement, le Setup.exe met à niveau la version de Windows Installer sur son ordinateur, si nécessaire, vérifie la signature numérique du package d’installation et installe le package sur son ordinateur.
-   Il existe un certificat numérique, MyCert. cer, fourni avec une clé privée, MyCert. pvk.
-   L’URL du site Web hypothétique visité par un client pour installer le package est https : \/ /www.blueyonderairlines.com/Products/MySetup/mysetup.html.
-   La disposition du serveur Web est la suivante. 

    | URL                                                               | Fichier        | Description                                    |
    |-------------------------------------------------------------------|-------------|------------------------------------------------|
    | https : \/ /www.blueyonderairlines.com/Products/mySetup/               | Setup.exe   | Programme d’amorçage Setup.exe.                        |
    | https : \/ /www.blueyonderairlines.com/Products/mySetup/               | MySetup.msi | Package d’installation                           |
    | https : \/ /www.blueyonderairlines.com/Products/mySetup/               | Cab1.cab    | Fichier cab source \# 1                        |
    | https : \/ /www.blueyonderairlines.com/Products/mySetup/               | Cab2.cab    | Fichier cab source \# 2                        |
    | https : \/ /www.blueyonderairlines.com/Products/Common/Instmsi/ANSI    | Instmsi.exe | redistribuable ANSI Windows Installer 2,0.    |
    | https : \/ /www.blueyonderairlines.com/Products/Common/Instmsi/Unicode | Instmsi.exe | redistribuable Unicode Windows Installer 2,0. |

    

     

[Continuer](configuring-the-setup-exe-resources.md)

 

 
