---
title: Fichier ACF
description: Le fichier ACF vous permet de personnaliser l’interface RPC de votre client et/ou de vos applications serveur sans affecter les caractéristiques du réseau de l’interface.
ms.assetid: 7d3fef5c-b645-4e10-b08d-b339025718b4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d234b30c25870dd7a21cb790cc4839236ab69093291285b64c870cf7c05cb11f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120080839"
---
# <a name="the-acf-file"></a>Fichier ACF

Le fichier ACF vous permet de personnaliser l’interface RPC de votre client et/ou de vos applications serveur sans affecter les caractéristiques du réseau de l’interface. Par exemple, si votre application cliente contient une structure de données complexe qui n’a qu’une signification sur l’ordinateur local, vous pouvez spécifier dans le fichier ACF comment les données de cette structure peuvent être représentées dans un format indépendant de l’ordinateur pour les appels de procédure distante.

Ce didacticiel illustre une autre utilisation du fichier ACF, en spécifiant le type de handle de liaison qui représente la connexion entre le client et le serveur. L' **\[** [**attribut \_ handle implicite**](/windows/desktop/Midl/implicit-handle) **\]** dans l’en-tête ACF permet à l’application cliente de sélectionner un serveur pour son appel de procédure distante. Le CCP définit le handle comme étant du handle de [**type \_ t**](/windows/desktop/Midl/handle-t) (un type de données primitif MIDL). Le compilateur MIDL insère le nom du handle de liaison spécifié par le ACF, Hello \_ IfHandle dans le fichier d’en-tête qu’il génère. Notez que ce fichier ACF particulier a un corps vide.

``` syntax
//file: hello.acf
[
    implicit_handle (handle_t hello_IfHandle)
] 
interface hello
{
}
```

Le compilateur MIDL a une option, [**/app \_ config**](/windows/desktop/Midl/-app-config), qui vous permet d’inclure certains attributs ACF, tels **que \_ descripteur implicite**, dans le fichier IDL, plutôt que de créer un fichier ACF distinct. Envisagez d’utiliser cette option si votre application n’a pas besoin de nombreuses configurations spéciales et si la compatibilité OSF stricte n’est pas un problème.

 

 