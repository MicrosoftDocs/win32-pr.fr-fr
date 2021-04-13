---
title: Contextes de rendu
description: Un contexte de rendu OpenGL est un port par le biais duquel toutes les commandes OpenGL passent. Chaque thread qui effectue des appels OpenGL doit avoir un contexte de rendu actuel. Les contextes de rendu lient OpenGL aux systèmes de fenêtrage Windows.
ms.assetid: 9fbbb0be-2db4-4bfc-9a5c-a43d71554abc
keywords:
- OpenGL sur Windows, contextes de rendu
- contextes de rendu OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53ac2ac6c5948da2b7372d600377666cd9e4e074
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310533"
---
# <a name="rendering-contexts"></a>Contextes de rendu

Un *contexte de rendu* OpenGL est un port par le biais duquel toutes les commandes OpenGL passent. Chaque thread qui effectue des appels OpenGL doit avoir un contexte de rendu actuel. Les contextes de rendu lient OpenGL aux systèmes de fenêtrage Windows.

Une application spécifie un contexte de périphérique Windows lorsqu’elle crée un contexte de rendu. Ce contexte de rendu est adapté au dessin sur l’appareil auquel le contexte de périphérique spécifié fait référence. En particulier, le contexte de rendu a le même format de pixel que le contexte de périphérique. Pour plus d’informations, consultez [rendu des fonctions de contexte](rendering-context-functions.md).

En dépit de cette relation, un contexte de rendu n’est pas le même qu’un contexte de périphérique. Un contexte de périphérique (Device Context) contient des informations pertinentes sur le composant Graphics (GDI) de Windows. Un contexte de rendu contient des informations pertinentes pour OpenGL. Un contexte de périphérique doit être spécifié explicitement dans un appel GDI. Un contexte de rendu est implicite dans un appel OpenGL. Vous devez définir le format de pixel d’un contexte de périphérique avant de créer un contexte de rendu.

Un thread qui effectue des appels OpenGL doit avoir un contexte de rendu actuel. Si une application effectue des appels OpenGL à partir d’un thread qui ne dispose pas d’un contexte de rendu actuel, rien ne se produit. l’appel n’a aucun effet. Une application crée généralement un contexte de rendu, la définit comme contexte de rendu actuel d’un thread, puis appelle des fonctions OpenGL. Lorsqu’il termine d’appeler les fonctions OpenGL, l’application dissocie le contexte de rendu du thread, puis supprime le contexte de rendu. Une fenêtre peut avoir plusieurs contextes de rendu dessinés à un moment donné, mais un thread ne peut avoir qu’un seul contexte de rendu actif en cours.

Un contexte de rendu en cours est associé à un contexte de périphérique. Ce contexte de périphérique n’a pas besoin d’être le même contexte de périphérique que celui utilisé lors de la création du contexte de rendu, mais il doit référencer le même appareil et avoir le même format de pixel.

Un thread ne peut avoir qu’un seul contexte de rendu actuel. Un contexte de rendu ne peut être actuel que pour un seul thread.

 

 




