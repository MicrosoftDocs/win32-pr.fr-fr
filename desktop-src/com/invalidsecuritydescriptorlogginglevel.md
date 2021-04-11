---
title: InvalidSecurityDescriptorLoggingLevel
description: Définit le niveau de détail des entrées du journal des événements sur les descripteurs de sécurité non valides pour le lancement et les autorisations d’accès des composants.
ms.assetid: 44f680b8-083d-44f0-a353-e66b87787ab7
keywords:
- Valeur de Registre InvalidSecurityDescriptorLoggingLevel COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25ac333a7cb8b54f383f93a71131cbb0a9314466
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309181"
---
# <a name="invalidsecuritydescriptorlogginglevel"></a>InvalidSecurityDescriptorLoggingLevel

Définit le niveau de détail des entrées du journal des événements sur les descripteurs de sécurité non valides pour le lancement et les autorisations d’accès des composants.

## <a name="registry-entry"></a>Entrée de Registre

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Ole
   InvalidSecurityDescriptorLoggingLevel = value
```

## <a name="remarks"></a>Notes

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

 

 




