---
title: Compilation MIDL
description: Compilation MIDL
ms.assetid: 2797ee3b-82fd-4cb5-9e95-23b2f2a8f011
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d6a94f94122aeeb1f2900c3adec7e567c794f31ee22259f657dfe5e95f3f688
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119047947"
---
# <a name="midl-compilation"></a>Compilation MIDL

À partir d’un fichier IDL, tel que [example2. idl](anatomy-of-an-idl-file.md), qui définit une ou plusieurs interfaces com et une bibliothèque de types, le compilateur MIDL (Midl.exe) génère les fichiers décrits dans le tableau suivant comme sortie par défaut.



| Nom de fichier                 | Description                                                                                                                                                                                           |
|--------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Example2. h<br/>    | Fichier d’en-tête, contenant les définitions de type et les déclarations de fonction pour toutes les interfaces définies dans le fichier IDL, ainsi que les déclarations anticipées pour les routines que les stubs appellent.<br/> |
| Example2 \_ p. c<br/> | Le fichier proxy/stub, qui comprend les points d’entrée de substitution pour les clients et pour les serveurs.<br/>                                                                                           |
| Example2 \_ i. c<br/> | Le fichier d’ID d’interface, qui définit le GUID pour chaque interface spécifiée dans le fichier IDL.<br/>                                                                                               |
| Example2. tlb<br/>  | Fichier de document composé qui contient des informations sur les types et les objets.<br/>                                                                                                                |
| Dlldata. c<br/>     | Contient les données dont vous avez besoin pour créer une DLL de proxy/stub.<br/>                                                                                                                                     |



 

Vous utilisez le fichier d’en-tête et tous les fichiers. c pour [créer une dll de proxy](building-and-registering-a-proxy-dll.md) pouvant prendre en charge l’interface lorsqu’elle est utilisée à la fois par les applications clientes et par les serveurs d’objets. Vous utilisez le fichier d’en-tête d’interface (example2. h) et le \_ fichier d’ID d’interface (example2 i. c) lors de la création du fichier exécutable pour une application cliente qui utilise l’interface. Vous pouvez choisir d’inclure le fichier de bibliothèque de types en tant que ressource dans votre fichier EXE ou DLL, ou vous pouvez l’envoyer en tant que fichier distinct.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Fichiers générés pour une interface COM](/windows/desktop/Midl/files-generated-for-a-com-interface)
</dt> <dt>

[Options du compilateur MIDL](midl-compiler-options.md)
</dt> </dl>

 

