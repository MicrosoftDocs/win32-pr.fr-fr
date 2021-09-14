---
description: L’écriture d’un fournisseur sécurisé requiert la prise en compte de l’hébergement du fournisseur, de la façon dont le fournisseur gère l’emprunt d’identité et de la vérification des droits d’accès aux données par les utilisateurs.
ms.assetid: 9a8b7730-cbb8-48fa-8a8f-8e551f00d20b
ms.tgt_platform: multiple
title: Sécurisation de votre fournisseur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b6b8fef1e90f09bc09488c058240b7fd1a88ebd
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127008199"
---
# <a name="securing-your-provider"></a>Sécurisation de votre fournisseur

L’écriture d’un fournisseur sécurisé requiert la prise en compte de l’hébergement du fournisseur, de la façon dont le fournisseur gère l’emprunt d’identité et de la vérification des droits d’accès aux données par les utilisateurs. Vous pouvez sécuriser les données dans votre espace de noms de fournisseur en exigeant l’authentification chiffrée des données avant leur envoi sur un réseau. Pour plus d’informations, consultez [la page exiger une connexion chiffrée à un espace de noms](requiring-an-encrypted-connection-to-a-namespace.md).

Si un utilisateur dispose d’un accès en **\_ écriture complet** dans n’importe quel espace de noms, l’utilisateur peut créer des abonnements à plusieurs espaces de noms pour les données d’un espace de noms dans lequel l’utilisateur est limité. Étant donné qu’un fournisseur peut être chargé dans n’importe quel espace de noms et s’exécuter dans n’importe quel contexte de sécurité, le fournisseur doit effectuer ses propres contrôles d’accès pour s’assurer que seuls les utilisateurs autorisés sont autorisés à accéder aux données ou à exécuter des méthodes. Pour plus d’informations, consultez [exécution de vérifications d’accès](performing-access-checks.md).

Les rubriques suivantes traitent de la sécurité du fournisseur :

-   [Hébergement et sécurité du fournisseur](provider-hosting-and-security.md)
-   [Exécution des vérifications d’accès](performing-access-checks.md)
-   [Clés de Registre pour le contrôle de la sécurité du fournisseur](registry-keys-for-controlling-provider-security-.md)
-   [Accès aux espaces de noms WMI](access-to-wmi-namespaces.md)
-   [Emprunt de l’identité d’un client](impersonating-a-client.md)

Les rubriques suivantes expliquent comment les clients et les scripts interagissent avec la sécurité du fournisseur :

-   [Configuration de l’authentification dans WMI](setting-authentication-in-wmi.md)
-   [Connexion entre différents systèmes d’exploitation](/windows/desktop/WmiSdk/troubleshooting-a-remote-wmi-connection)
-   [Définition du niveau de sécurité de processus par défaut à l’aide de VBScript](setting-the-default-process-security-level-using-vbscript.md)
-   [Définition de la sécurité des processus d’application cliente](setting-client-application-process-security.md)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Maintenance de la sécurité WMI](maintaining-wmi-security.md)
</dt> <dt>

[Utilisation de WMI](using-wmi.md)
</dt> </dl>

 

 
