---
description: Toutes les applications COM+ peuvent être exposées en tant que service Web XML.
ms.assetid: 03c3d5a7-eb98-4916-b6ef-ef6aac86c574
title: Création de services Web XML
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b10652531e64fec38f2ac221184cb589a27b343d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106516781"
---
# <a name="creating-xml-web-services"></a>Création de services Web XML

Toutes les applications COM+ peuvent être exposées en tant que service Web XML. Les méthodes des interfaces par défaut des composants d’applications configurés (composants dans le catalogue COM+ serveurs) peuvent ensuite être appelées à distance. Vous pouvez utiliser l’outil d’administration Services de composants pour créer un répertoire racine virtuel IIS à partir duquel les méthodes de composant peuvent être appelées à l’aide de SOAP.

> [!Note]  
> Le .NET Framework doit être installé sur votre ordinateur afin d’exposer une application COM+ en tant que service Web XML.

 

**Pour exposer une application COM+ en tant que service Web XML**

1.  Dans l’arborescence de la console de l’outil d’administration Services de composants, sous **services de composants**, ouvrez le dossier **applications com+** associé à l’ordinateur que vous souhaitez gérer.

2.  Cliquez avec le bouton droit sur l’application que vous souhaitez exposer en tant que service Web XML, puis choisissez **Propriétés**.

3.  Dans la boîte de dialogue Propriétés, cliquez sur l’onglet **activation** .

4.  Activez la case à cocher **utilise le protocole SOAP** .

5.  Dans la zone de texte **vroot SOAP** , entrez le nom du répertoire racine virtuel IIS à partir duquel vous pouvez accéder à distance aux méthodes des composants. Notez qu’un VRoot SOAP ne peut pas être un sous-répertoire d’un autre répertoire VRoot SOAP.

6.  Cliquez sur **OK**.

    Si vous spécifiez le répertoire racine virtuel IIS en tant que *vroot* et si le nom de domaine complet de votre serveur est *ServerName*, l’URL où votre composant est exposé en tant que service Web XML est https://*ServerName* / *vroot*/.

    Le répertoire correspondant dans votre système de fichiers est \\ Windows \\ system32 \\ com \\ SoapVRoots \\ *vroot* \\ ; COM+ place plusieurs fichiers de configuration et des programmes ASP.NET. Pour un service Web XML soumis à une charge importante, vous pouvez ajuster les paramètres stockés dans le web.config de fichiers. Pour plus d’informations sur ce fichier, consultez la documentation d’IIS.

    Les paramètres de sécurité par défaut d’une application COM+ exposée en tant que service Web XML varient en fonction de la version du .NET Framework installée. Si la version 1,0 est installée, les services Web XML ne sont pas sécurisés par défaut. tous les appels sont acceptés et aucun chiffrement n’est utilisé. Si la version 1,1 ou une version ultérieure est installée, les services Web XML sont sécurisés par défaut. les appelants doivent être authentifiés et le chiffrement est requis.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Accès aux services Web XML en mode CAO](accessing-xml-web-services-in-cao-mode.md)
</dt> <dt>

[Accès aux services Web XML en mode WKO](accessing-xml-web-services-in-wko-mode.md)
</dt> <dt>

[Vue d’ensemble du service SOAP COM+](com--soap-service-overview.md)
</dt> <dt>

[Sécurisation des services Web XML](securing-xml-web-services.md)
</dt> </dl>

 

 



