---
title: Objets de données de serveur
description: L’API SDO (Server Data Objects) permet de configurer et d’administrer par programme un système exécutant NPS.
ms.assetid: 9d159e15-f534-4ab1-9641-db70064beb51
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6eebd0f837f9a8a36af1eb9118189015e677e2af
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "106509451"
---
# <a name="server-data-objects"></a>Objets de données de serveur

> [!Note]  
> Le service d’authentification Internet (IAS) a été renommé serveur NPS (Network Policy Server) à partir de Windows Server 2008. Le contenu de cette rubrique s’applique à IAS et à NPS. Dans le texte, NPS est utilisé pour faire référence à toutes les versions du service, y compris les versions initialement appelées IAS.

 

L’API SDO (Server Data Objects) permet de configurer et d’administrer par programme un système exécutant NPS. À l’aide de SDO, un développeur peut également écrire des applications qui administrent les stratégies d’accès à distance et les profils. Les stratégies et les profils d’accès à distance sont utilisés par le service de routage et d’accès à distance (RRAS), ainsi que par le serveur NPS pour déterminer si un client distant est autorisé à se connecter à un serveur d’accès réseau (NAS).

L’API SDO est applicable dans n’importe quel environnement qui utilise des stratégies d’accès à distance ou NPS.

Avec l’API SDO, un développeur peut manipuler tout élément de la configuration NPS qui est accessible via l’interface utilisateur du serveur NPS.

L’API SDO permet également de définir ou de récupérer les valeurs accessibles via la page de propriétés paramètres de numérotation utilisateur.

L’API SDO est composée d’interfaces COM. Chacune des interfaces de l’API SDO hérite de l’interface COM [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . L’interface **IDispatch** permet aux développeurs d’appeler les méthodes d’interface SDO à partir de Visual Basic ou de n’importe quel client Automation, ainsi qu’à partir de C/C++.

Les développeurs peuvent également appeler l’API SDO à partir de langages de script tels que VBScript. Toutefois, étant donné que VBScript est limité à l’utilisation des paramètres de type VARIANT uniquement, les fonctionnalités de SDO ne sont pas toutes disponibles.

## <a name="in-this-section"></a>Dans cette section

[Vue d’ensemble](/windows/desktop/Nps/sdo-about-server-data-objects)

Informations générales sur l’API des objets de données du serveur.

[À](/windows/desktop/Nps/sdo-using-server-data-objects)

Exemple de code qui montre comment utiliser l’API des objets de données du serveur.

[Référence](/windows/desktop/Nps/sdo-server-data-objects-reference)

Documentation des types énumérés et des interfaces qui composent l’API des objets de données du serveur.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Serveur de stratégie réseau (service d’authentification Internet)](portal.md)
</dt> <dt>

[Service d’accès à distance](/windows/desktop/RRAS/portal)
</dt> </dl>

 

 