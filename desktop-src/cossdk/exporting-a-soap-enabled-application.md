---
description: Lorsque vous utilisez COM+ pour créer un service Web XML, ce service peut être utilisé par n’importe quel client autorisé, y compris ceux qui n’utilisent pas COM+ ou même Microsoft Windows.
ms.assetid: c40031a6-f3de-4ef4-b9aa-3f49e57da5b4
title: Exportation d’une application SOAP-Enabled
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce79bbc5dca59feb23ba9e976575b3b33570ecd27cf1e6a68560b02e073f48bc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118307286"
---
# <a name="exporting-a-soap-enabled-application"></a>Exportation d’une application SOAP-Enabled

Lorsque vous utilisez COM+ pour créer un service Web XML, ce service peut être utilisé par n’importe quel client autorisé, y compris ceux qui n’utilisent pas COM+ ou même Microsoft Windows. Toutefois, l’utilisation d’un service Web COM+ en mode CAO (client-Activated Object) à partir d’une application cliente COM+ est particulièrement simple. Exportez simplement l’application compatible SOAP en mode proxy, puis [importez](importing-a-soap-enabled-application.md) -la dans le client pour lequel vous souhaitez accéder au service Web XML correspondant.

## <a name="component-services-administrative-tool"></a>Outil d’administration Services de composants

Pour exporter une application compatible SOAP à partir d’un serveur, procédez comme suit :

1.  Dans l’arborescence de la console de l’outil d’administration Services de composants, sous **services de composants**, ouvrez le dossier **applications com+** associé à l’ordinateur que vous souhaitez gérer.

2.  Cliquez avec le bouton droit sur le composant que vous souhaitez exposer en tant que service Web XML, puis choisissez **Exporter**. L' **Assistant exportation d’application com+** s’affiche.

3.  Dans la zone de texte intitulée **Entrez le chemin d’accès complet et le nom du fichier d’application à créer**, entrez le chemin d’accès complet et le nom du fichier MSI qui contiendra l’application exportée, ou cliquez sur **Parcourir** pour sélectionner le chemin d’accès complet et le nom de fichier à l’aide d’une boîte de dialogue.

4.  Sous **Exporter en tant que**, sélectionnez la case **d’option proxy d’application-installer sur d’autres ordinateurs pour activer l’accès à cet ordinateur** .

## <a name="visual-basic"></a>Visual Basic

Non applicable.

## <a name="cc"></a>C/C++

Non applicable.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Vue d’ensemble du service SOAP COM+](com--soap-service-overview.md)
</dt> <dt>

[Création de services Web XML](creating-xml-web-services.md)
</dt> <dt>

[Importation d’une application SOAP-Enabled](importing-a-soap-enabled-application.md)
</dt> </dl>

 

 



