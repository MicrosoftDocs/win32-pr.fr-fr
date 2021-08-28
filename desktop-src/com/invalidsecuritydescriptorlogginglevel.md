---
title: InvalidSecurityDescriptorLoggingLevel
description: Définit le niveau de détail des entrées du journal des événements sur les descripteurs de sécurité non valides pour le lancement et les autorisations d’accès des composants.
ms.assetid: 44f680b8-083d-44f0-a353-e66b87787ab7
keywords:
- Valeur de Registre InvalidSecurityDescriptorLoggingLevel COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c2362b38c19acd8d895e5fa9640475fa401a7d5bd88c8016056df2d22c3a579
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119854339"
---
# <a name="invalidsecuritydescriptorlogginglevel"></a>InvalidSecurityDescriptorLoggingLevel

Définit le niveau de détail des entrées du journal des événements sur les descripteurs de sécurité non valides pour le lancement et les autorisations d’accès des composants.

## <a name="registry-entry"></a>Entrée de Registre

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Ole
   InvalidSecurityDescriptorLoggingLevel = value
```

## <a name="remarks"></a>Remarques

Il s’agit d’une valeur de **Registre \_ DWORD** .



| Valeur | Description                                                                                                                                                                    |
|-------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 1     | Consigne toujours les échecs quand COM détecte un descripteur de sécurité non valide. Il s’agit de la valeur par défaut.                                                                                  |
| 2     | Ne consigne jamais les échecs quand COM détecte un descripteur de sécurité non valide. Il n’est pas recommandé de désactiver la journalisation des événements, car cela peut compliquer le diagnostic des problèmes. |



 

Si vous définissez directement les descripteurs de sécurité des autorisations d’exécution et d’accès (généralement appelées ACL), il est possible de construire un descripteur de sécurité dont la signification ne peut pas être interprétée sans ambiguïté. COM crée une entrée dans le journal des événements lorsqu’il rencontre un descripteur de sécurité non valide.

Notez que [**ActivationFailureLoggingLevel**](activationfailurelogginglevel.md) et [**CallFailureLoggingLevel**](callfailurelogginglevel.md) n’ont aucun contrôle sur la journalisation des erreurs de descripteur de sécurité non valides. Utilisez **InvalidSecurityDescriptorLoggingLevel** pour un contrôle total de cette fonctionnalité.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Définition de la sécurité pour les applications COM](setting-security-for-com-applications.md)
</dt> </dl>

 

 




