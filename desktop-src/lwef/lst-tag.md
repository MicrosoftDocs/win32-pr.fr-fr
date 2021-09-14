---
title: Balise LST
description: Balise LST
ms.assetid: 82246675-9aa1-4603-a8f7-a5fd7b3f6be2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ecf13da7bf0267941939ec22c12706ed8c75c27e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127296406"
---
# <a name="lst-tag"></a>Balise LST

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descriptive**
</dt> <dd>

Répète la dernière instruction orale pour le caractère.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Stockéesyntaxe**
</dt> <dd>

\\**LST**\\

</dd> </dl>

### <a name="remarks"></a>Notes

Cette balise permet à un caractère de répéter sa dernière instruction orale. Cette balise doit apparaître seule dans la méthode [**Speak**](speak-method.md) ; aucun autre texte ou paramètre ne peut être inclus. Lorsque le texte parlé est répété, toutes les autres balises incluses dans le texte d’origine sont répétées, à l’exception des signets. Aux. WAV et. Les fichiers LWV inclus dans le texte sont également répétés.

 

 




