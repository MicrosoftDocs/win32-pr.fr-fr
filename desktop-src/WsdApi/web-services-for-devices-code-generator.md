---
description: Utilitaire de ligne de commande qui génère du code de programme à partir d’une description de service.
ms.assetid: 76dffca8-bb84-4384-a9e8-120a4cf2acac
title: Générateur de code des services Web sur les appareils
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b214fd51468dd3cf46c2625ae0e493851ef90f38b7fea0f64a3973f068be5253
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119382269"
---
# <a name="web-services-on-devices-code-generator"></a>Générateur de code des services Web sur les appareils

Le générateur de code des services Web sur les appareils, WsdCodeGen, est un utilitaire de ligne de commande qui génère du code de programme à partir d’une description de service. La description du service est stockée dans des fichiers WSDL et/ou XSD. WsdCodeGen crée des fichiers C++ et IDL (Interface Definition Language). Les développeurs peuvent utiliser WsdCodeGen pour créer des applications WSDAPI sans se soucier de la façon dont les données sont marshalées et représentées sur le câble.

WsdCodeGen peut être utilisé pour générer du code pour un service, un client ou les deux. L’utilitaire génère du code stub pour les services, le code proxy pour les clients, et l’interface et le code de type pour les deux.

cet outil est disponible dans le kit de développement logiciel (SDK) de Microsoft Windows et dans le kit WDK (Windows Driver kit). Les outils du kit de développement logiciel se trouvent dans le répertoire suivant : <Windows SDK Install Folder> \\ bin.

le SDK Windows comprend un exemple de code généré par WsdCodeGen. Pour plus d’informations, consultez [exemples wsdapi](wsdapi-samples.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[À propos de WsdCodeGen](about-wsdcodegen.md)
</dt> <dt>

[Utilisation de WsdCodeGen](using-wsdcodegen.md)
</dt> <dt>

[Référence WsdCodeGen](wsdcodegen-reference.md)
</dt> <dt>

[Développement d’applications WSD sur Windows](wsd-application-development-on-windows.md)
</dt> </dl>

 

 



