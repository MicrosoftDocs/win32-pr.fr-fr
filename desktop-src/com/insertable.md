---
title: Insertable (clé CLSID)
description: Indique que les objets de cette classe doivent apparaître dans la zone de liste de la boîte de dialogue Insérer un objet lorsqu’ils sont utilisés par les applications de conteneur COM.
ms.assetid: 908cbfc4-ebf8-454e-b2e5-34449de60e7f
keywords:
- Clé de Registre Insertable COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 699de5db82981e5f0f1db1229d31f96620adcb8c
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122884315"
---
# <a name="insertable-clsid-key"></a>Insertable (clé CLSID)

Indique que les objets de cette classe doivent apparaître dans la zone de liste de la boîte de dialogue **Insérer un objet** lorsqu’ils sont utilisés par les applications de conteneur com.

## <a name="registry-entry"></a>Entrée de Registre

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      Insertable
```

## <a name="remarks"></a>Remarques

Cette clé est une entrée obligatoire pour les applications COM 32 bits dont les objets peuvent être insérés dans des applications 16 bits existantes. Les applications 16 bits existantes recherchent dans le registre cette clé, qui informe l’application que le serveur prend en charge les incorporations. Si la clé pouvant être **insérée** existe, les applications 16 bits peuvent également essayer de vérifier que le serveur existe sur l’ordinateur. les applications 16 bits récupèrent généralement la valeur de la clé [**LocalServer**](localserver.md) de la classe et vérifient s’il s’agit d’un fichier valide sur le système. Par conséquent, pour qu’une application 32 bits soit à pouvoir être insérée par une application 16 bits, l’application 32 bits doit inscrire la sous-clé **LocalServer** en plus de l’inscription [**LocalServer32**](localserver32.md).

Utilisé avec les contrôles, cette entrée indique qu’un objet peut agir uniquement comme un objet incorporé sur place sans fonctionnalités de contrôle spéciales. Les objets qui ont cette clé s’affichent dans la boîte de dialogue **Insérer un objet** pour leur conteneur. Lorsqu’elle est utilisée avec les contrôles, cette entrée indique également que le contrôle a été testé avec des conteneurs sans contrôle. Cette entrée est également facultative et peut être omise lorsqu’un contrôle n’est pas conçu pour fonctionner avec des conteneurs plus anciens qui ne comprennent pas de contrôles.

> [!Note]  
> Cette clé n’est pas présente pour les classes internes comme les classes moniker.

 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**&lt;ProgID&gt;**](-progid--key.md)
</dt> </dl>

 

 




