---
title: Clé CLSID
description: Un CLSID est un identificateur global unique qui identifie un objet de classe COM. Si votre serveur ou conteneur autorise la liaison à ses objets incorporés, vous devez inscrire un CLSID pour chaque classe d’objets prise en charge.
ms.assetid: b5777d87-abf2-45b9-9d95-61db878a5810
keywords:
- Clé de Registre CLSID COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd390fc6a1ccb15e128245c3b6a80e2b4ca57f41de9e9c21e93ebe4c708783d0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119854979"
---
# <a name="clsid-key"></a>Clé CLSID

Un CLSID est un identificateur global unique qui identifie un objet de classe COM. Si votre serveur ou conteneur autorise la liaison à ses objets incorporés, vous devez inscrire un CLSID pour chaque classe d’objets prise en charge.

## <a name="registry-key"></a>Clé de Registre

**HKEY \_ Classe de logiciels de l' \_ ordinateur local \\ \\ \\ CLSID** \\ *{* CLSID *}*



| Clé de Registre                                                 | Description                                                                                                                              |
|--------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| [**AppID**](appid.md)                                       | Associe un AppID à un CLSID.                                                                                                        |
| [**AutoConvertTo**](autoconvertto.md)                       | Spécifie la conversion automatique d’une classe d’objets donnée en une nouvelle classe d’objets.                                                |
| [**Traitement autotraité**](autotreatas.md)                           | Définit automatiquement le CLSID de la clé [**TreatAs**](treatas.md) sur la valeur spécifiée.                                              |
| [**AuxUserType**](auxusertype.md)                           | Spécifie le nom complet et les noms d’application de l’application.                                                                     |
| [**Contrôler**](control.md)                                   | identifie un objet en tant que contrôle ActiveX.                                                                                              |
| [**Conversion**](conversion.md)                             | Utilisé par la boîte de dialogue **convertir** pour déterminer les formats qu’une application peut lire et écrire.                                           |
| [**DataFormats**](dataformats.md)                           | Spécifie les formats de données par défaut et principaux pris en charge par une application.                                                                 |
| [**DefaultIcon**](defaulticon.md)                           | Fournit des informations sur l’icône par défaut pour les présentations sous forme d’objets.                                                                   |
| [**InprocHandler**](inprochandler.md)                       | Spécifie si une application utilise un gestionnaire personnalisé.                                                                                  |
| [**InprocHandler32**](inprochandler32.md)                   | Spécifie si une application utilise un gestionnaire personnalisé.                                                                                  |
| [**InprocServer**](inprocserver.md)                         | Spécifie le chemin d’accès à la DLL du serveur in-process.                                                                                         |
| [**InprocServer32**](inprocserver32.md)                     | Inscrit un serveur in-process 32 bits et spécifie le modèle de thread du cloisonnement sur lequel le serveur peut s’exécuter.                           |
| [**Insertable**](insertable.md)                             | Indique que les objets de cette classe doivent apparaître dans la zone de liste de la boîte de dialogue **Insérer un objet** lorsqu’ils sont utilisés par les applications de conteneur com. |
| [**Interface**](interface.md)                               | Entrée facultative qui spécifie tous les ID d’interface (IID) pris en charge par la classe associée.                                             |
| [**LocalServer**](localserver.md)                           | Spécifie le chemin d’accès complet à une application serveur locale 16 bits.                                                                            |
| [**LocalServer32**](localserver32.md)                       | Spécifie le chemin d’accès complet à une application serveur locale 32 bits.                                                                            |
| [**MiscStatus**](miscstatus.md)                             | Spécifie comment créer et afficher un objet.                                                                                           |
| [**ProgID**](progid.md)                                     | Associe un ProgID à un CLSID.                                                                                                        |
| [**ToolBoxBitmap32**](toolboxbitmap32.md)                   | Identifie le nom de module et l’ID de ressource pour une image bitmap de 16 x 16 à utiliser pour la face d’un bouton de barre d’outils ou de boîte à outils.                      |
| [**TreatAs**](treatas.md)                                   | Spécifie le CLSID d’une classe qui peut émuler la classe actuelle.                                                                       |
| [**DoVerb**](verb.md)                                         | Spécifie les verbes à inscrire pour une application.                                                                                 |
| [**Version**](version.md)                                   | Spécifie le numéro de version du contrôle.                                                                                             |
| [**VersionIndependentProgID**](versionindependentprogid.md) | Associe un ProgID à un CLSID. Cette valeur est utilisée pour déterminer la version la plus récente d’une application d’objet.                           |



 

## <a name="remarks"></a>Remarques

La clé de classes de logiciels de l' **\_ \_ ordinateur \\ \\ local HKEY** correspond à la clé **\_ \_ racine HKEY classes** , qui a été conservée pour la compatibilité avec les versions antérieures de com.

La clé CLSID contient les informations utilisées par le gestionnaire COM par défaut pour retourner les informations relatives à une classe lorsqu’elle est à l’État en cours d’exécution.

Pour obtenir un CLSID pour votre application, vous pouvez utiliser la Uuidgen.exe ou utiliser la fonction [**CoCreateGuid**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateguid) .

Le CLSID est un nombre 128 bits, en hexadécimal, au sein d’une paire d’accolades.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**CoCreateGuid**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateguid)
</dt> </dl>

 

 




