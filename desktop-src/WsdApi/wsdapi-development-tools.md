---
description: les outils de développement WSDAPI inclus dans le SDK Windows (wsd CodeGen, l’hôte de débogage wsd et le Client de débogage wsd) permettent aux développeurs de créer et de déboguer des périphériques et des clients WSDAPI.
ms.assetid: 8bf6424e-1eed-4b0a-9d56-7aaf03a47992
title: Outils de développement WSDAPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd245e347cab6205a8883126dcae281646a3488f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127013045"
---
# <a name="wsdapi-development-tools"></a>Outils de développement WSDAPI

les outils de développement WSDAPI inclus dans le SDK Windows (wsd CodeGen, l’hôte de débogage wsd et le Client de débogage wsd) permettent aux développeurs de créer et de déboguer des périphériques et des clients WSDAPI. Le code source de ces outils n’est pas disponible. Les outils du kit de développement logiciel se trouvent dans le répertoire suivant : <Windows SDK Install Folder> \\ bin.

WSD CodeGen (wsdcodegen.exe) convertit un contrat WSDL en code C++ généré, que les développeurs peuvent appeler directement dans. Il gère la sérialisation des données et la représentation filaire afin que les développeurs puissent se concentrer sur la conception d’applications. Pour plus d’informations sur WSD CodeGen, consultez [Web Services on Devices Code Generator](web-services-for-devices-code-generator.md). cet outil est disponible dans le kit de développement logiciel (SDK) de Microsoft Windows et dans le kit WDK (Windows Driver kit).

Les outils de débogage de l’hôte de débogage WSD (wsddebug \_host.exe) et du client de débogage WSD (wsddebug \_client.exe) aident les développeurs à déboguer leurs clients et hôtes. Ces outils peuvent être utilisés pour vérifier et inspecter les WS-Discovery et le trafic d’échange de métadonnées. Pour plus d’informations sur l’hôte de débogage WSD et le client de débogage WSD, consultez [outils de débogage](debugging-tools.md). ces outils sont disponibles uniquement dans le SDK Windows.

Il existe un outil de développement supplémentaire, nommé [wsdapi Basic Interoperability Tool (WSDBIT)](https://msdn.microsoft.com/library/cc264250.aspx), qui est disponible uniquement dans le kit WDK. Cet outil est utilisé pour tester les méthodes de service, MTOM (Message Transmission Optimization Mechanism), les pièces jointes ou WS-Eventing.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Développement d’applications WSD sur Windows](wsd-application-development-on-windows.md)
</dt> <dt>

[Générateur de code des services Web sur les appareils](web-services-for-devices-code-generator.md)
</dt> <dt>

[Outil d’interopérabilité de base WSDAPI (WSDBIT)](https://msdn.microsoft.com/library/cc264250.aspx)
</dt> <dt>

[Outils de débogage](debugging-tools.md)
</dt> </dl>

 

 



