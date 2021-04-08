---
title: Les interfaces IADs et IDirectoryObject
description: Les clients ADSI gèrent et manipulent des objets de service d’annuaire à l’aide de l’une des deux interfaces COM IADs ou IDirectoryObject.
ms.assetid: f9c486b0-3dfb-4abf-afbf-08749e04315f
ms.tgt_platform: multiple
keywords:
- IADs ADSI, à propos de
- IDirectoryObject ADSI, à propos de
- ADSI ADSI, avec les interfaces, IADs et IDirectoryObject
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 32dfef47fe1c66e4303725deecec14fe93d1fd92
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "103842737"
---
# <a name="the-iads-and-idirectoryobject-interfaces"></a>Les interfaces IADs et IDirectoryObject

Les clients ADSI gèrent et manipulent des objets de service d’annuaire à l’aide de l’une des deux interfaces COM suivantes : [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) ou [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject). **IADs** est une interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) destinée à être utilisée par des clients à liaison tardive tels que ceux écrits en Microsoft Visual Basic, Java et divers langages de script. **IDirectoryObject** est une interface vtable qui fournit un accès direct aux objets par des clients à liaison anticipée, tels que ceux écrits en C et C++.

Chaque objet ADSI doit implémenter à la fois [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) et [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject). Les clients ADSI écrits dans des langages tels que C ou C++, qui sont en mesure d’accéder directement aux vtables, peuvent utiliser l’une ou l’autre interface, mais pas les deux dans la même application. Les clients ADSI écrits en Visual Basic ou Java sont limités à l’utilisation de **IADs**.

L’interface [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) permet aux clients à liaison tardive de tirer parti des fonctionnalités de maintenance inhérentes du modèle d’objet ADSI. Parmi ces fonctionnalités, citons le cache des propriétés, qui permet aux clients de lire et d’écrire des propriétés sans passer par le câble pour chaque appel. En outre, les applications clientes tirent parti de l’interface utilisateur et des bibliothèques de contrôles ActiveX puissantes, ainsi qu’un style de programmation plus simple. En retour, les clients à liaison tardive doivent utiliser le type de données **Variant** , qui exclut l’utilisation des types de données natifs plus riches fournis par ADSI.

L’interface [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) permet aux clients à liaison anticipée de tirer pleinement parti des types de données du service d’annuaire natif au détriment d’un léger avantage en termes de performances par rapport à l’utilisation du cache de propriétés. En retour, l’interface **IDirectoryObject** fournit un accès direct et direct aux propriétés de l’objet par le biais d’une requête unique, plutôt qu’à l’aide d’appels d' **extraction** et de **placement** individuels.

 

 