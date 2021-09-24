---
description: cette rubrique décrit les limites de mémoire pour les versions Windows et Windows Server prises en charge.
ms.assetid: de09c8af-0ed8-4fd4-b8e8-2c921aafe6f2
title: Limites de mémoire pour les versions de Windows et de Windows Server
ms.topic: article
ms.date: 09/10/2021
ms.openlocfilehash: c53c6f1c805cdf92bdaf066cccf017044c5f8912
ms.sourcegitcommit: 2c13d0f1620f7c089687ef1d97e8c1d22e5d537a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "128519915"
---
# <a name="memory-limits-for-windows-and-windows-server-releases"></a>Limites de mémoire pour les versions de Windows et de Windows Server

cette rubrique décrit les limites de mémoire pour les versions Windows et Windows Server prises en charge.

Les limites de la mémoire et de l’espace d’adressage varient en fonction de la plateforme, du système d’exploitation et de l’utilisation de la valeur de **\_ \_ grande \_ adresse \_ sensible au fichier image** de la structure d' [**\_ image chargée**](/windows/win32/api/dbghelp/ns-dbghelp-loaded_image) et du [réglage à 4 gigaoctets](4-gigabyte-tuning.md) (4GT). **Image \_ La prise en \_ \_ \_ charge d’adresses volumineuses** est définie ou effacée à l’aide de l’option de l’éditeur de liens [/LARGEADDRESSAWARE](/cpp/build/reference/largeaddressaware-handle-large-addresses?view=vs-2019) .

le réglage à 4 gigaoctets (4GT), également appelé réglage de la mémoire de l’application, ou le commutateur/3GB, est une technologie (applicable uniquement aux systèmes 32 bits) qui modifie la quantité d’espace d’adressage virtuel disponible pour les applications en mode utilisateur. L’activation de cette technologie réduit la taille globale de l’espace d’adressage virtuel du système et, par conséquent, les valeurs maximales des ressources système. Pour plus d’informations, voir [qu’est-ce que 4GT]( /previous-versions/windows/it-pro/windows-server-2003/cc786709(v=ws.10)).

les limites de la mémoire physique pour les plateformes 32 bits dépendent également de l' [Extension d’adresse physique](physical-address-extension.md) (PAE), qui permet aux systèmes de Windows 32 bits d’utiliser plus de 4 go de mémoire physique.

## <a name="memory-and-address-space-limits"></a>Mémoire et limites de l’espace d’adressage

Le tableau suivant spécifie les limites de la mémoire et de l’espace d’adressage pour les versions prises en charge de Windows. Sauf indication contraire, les limites indiquées dans ce tableau s’appliquent à toutes les versions prises en charge.



| Type de mémoire                                                                                   | Limite sur x86                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    | Limite en Windows de 64 bits                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Espace d’adressage virtuel en mode utilisateur pour chaque processus 32 bits<br/>                            | 2 Go<br/> Jusqu’à 3 Go avec prise en **\_ \_ \_ \_ charge d’adresses volumineuses avec fichier image** et 4GT<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       | 2 Go avec prise en charge d’une **\_ \_ grande \_ adresse \_ de fichier image** effacée (par défaut)<br/> 4 Go avec prise en charge de l' **\_ \_ \_ \_ adresse importante du fichier image**<br/>                                                                                                                                                                                                                                                                                                                                                                 |
| Espace d’adressage virtuel en mode utilisateur pour chaque processus 64 bits<br/>                            | Non applicable<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              | **Avec image \_ FICHIER avec prise en \_ \_ \_ charge d’adresses volumineuses** (par défaut) :<br/> **x64 : Windows 8.1 et Windows Server 2012 R2 ou version ultérieure :** 128 to<br/> **x64 : Windows 8 et Windows Server 2012 ou une version antérieure** de 8 to<br/> **Systèmes Intel Itanium :** 7 to<br/> <br/> 2 Go avec prise en charge d’une **\_ \_ grande \_ adresse \_ de fichier image** effacée<br/>                                                                                                                                                                                              |
| Espace d’adressage virtuel en mode noyau<br/>                                                  | 2 Go<br/> De 1 Go à un maximum de 2 Go avec 4GT<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              | **Windows 8.1 et Windows Server 2012 R2 ou version ultérieure :** 128 to<br/> **Windows 8 et Windows Server 2012 ou une version antérieure** de 8 to <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| Pool paginé<br/>                                                                         | 384 Go ou limite de validation du système, la valeur la plus petite étant retenue. **Windows 8.1 et Windows Server 2012 R2 :** 15,5 to ou limite de validation du système, la valeur la plus petite étant retenue. <br/> **Windows server 2008 R2, Windows 7, Windows Server 2008 et Windows Vista :** Limité par l’espace d’adressage virtuel en mode noyau disponible. à compter de Windows Vista avec Service Pack 1 (SP1), la réserve paginée peut également être limitée par la valeur de clé de registre [PagedPoolLimit](memory-management-registry-keys.md) .<br/> **Windows serveur d’hébergement et Windows server 2003 :** 530 mo<br/> **Windows XP :** 490 mo<br/> <br/>                                                                                                 | 384 go ou limite de validation système, selon la valeur la plus petite **Windows 8.1 et Windows Server 2012 R2 :** 15,5 to ou la limite de validation du système, la valeur la plus petite étant retenue. <br/> **Windows server 2008 R2, Windows 7, Windows server 2008 et Windows Vista :** 128 go ou limite de validation du système, la valeur la plus petite étant retenue<br/> **Windows Server 2003 et Windows XP :** Jusqu’à 128 Go en fonction de la configuration et de la RAM.<br/> <br/>                                                                                |
| Pool non paginé<br/>                                                                      | 75% de RAM ou 2 Go, la valeur la plus petite étant retenue. **Windows 8.1 et Windows Server 2012 R2 :** ram ou 16 to, selon la valeur la plus petite (l’espace d’adressage est limité à 2 x ram).<br/> **Windows Vista :** Limité uniquement par l’espace d’adressage virtuel et la mémoire physique en mode noyau. à partir de Windows Vista avec SP1, la réserve non paginée peut également être limitée par la valeur de clé de registre [NonPagedPoolLimit](memory-management-registry-keys.md) .<br/> **Windows serveur d’hébergement, Windows server 2003 et Windows XP :** 256 mo ou 128 mo avec 4gt.<br/> <br/>                                                                                                                                                 | ram ou 128 go, selon la valeur la plus petite (l’espace d’adressage est limité à 2 x RAM) **Windows 8.1 et Windows Server 2012 R2 :** ram ou 16 to, selon la valeur la plus petite (l’espace d’adressage est limité à 2 x ram).<br/> **Windows server 2008 R2, Windows 7 et Windows Server 2008 :** 75% de RAM, jusqu’à un maximum de 128 go<br/> **Windows Vista :** 40% de RAM, jusqu’à un maximum de 128 go.<br/> **Windows Server 2003 et Windows XP :** Jusqu’à 128 Go en fonction de la configuration et de la RAM.<br/> <br/> |
| Espace d’adressage virtuel du cache système (taille physique limitée uniquement par la mémoire physique)<br/> | Limité par l’espace d’adressage virtuel en mode noyau disponible ou la valeur de clé de Registre [SystemCacheLimit](memory-management-registry-keys.md) .<br/> **Windows 8.1 et Windows Server 2012 R2 :** 16 to.<br/> **Windows Vista :** Limité uniquement par l’espace d’adressage virtuel en mode noyau. à compter de Windows Vista avec SP1, l’espace d’adressage virtuel de la mémoire cache du système peut également être limité par la valeur de clé de registre [SystemCacheLimit](memory-management-registry-keys.md) .<br/> **Windows serveur d’hébergement, Windows server 2003 et Windows XP :** 860 mo avec la clé de registre [LargeSystemCache](/previous-versions/windows/it-pro/windows-server-2003/cc784562(v=ws.10)) définie et sans 4gt ; jusqu’à 448 Mo avec 4GT.<br/> <br/> | toujours 1 to, quelle que soit la RAM physique **Windows 8.1 et Windows Server 2012 R2 :** 16 to.<br/> **Windows Server 2003 et Windows XP :** Jusqu’à 1 to en fonction de la configuration et de la RAM.<br/> <br/>                                                                                                                                                                                                                                                                                            |



 

## <a name="physical-memory-limits-windows-10"></a>Limites de la mémoire physique : Windows 10

Le tableau suivant spécifie les limites de la mémoire physique pour Windows 10.



| Version               | Limite sur x86    | Limite sur x64     |
|-----------------------|-----------------|------------------|
| Windows 10 Entreprise | 4 Go<br/> | 6 To<br/>   |
| Windows 10 Éducation  | 4 Go<br/> | 2 To<br/>   |
| Windows 10 Professionnel pour les Stations de travail  | 4 Go<br/> | 6 To<br/>   |
| Windows 10 Professionnel        | 4 Go<br/> | 2 To<br/>   |
| Windows 10 Famille       | 4 Go<br/> | 128 Go<br/> |



 

## <a name="physical-memory-limits-windows-server-2016"></a>Limites de la mémoire physique : Windows Server 2016

Le tableau suivant spécifie les limites de la mémoire physique pour Windows Server 2016.



| Version                        | Limite sur x64     |
|--------------------------------|------------------|
| Windows Server 2016 Datacenter | 24 To<br/> |
| Windows Server 2016 Standard   | 24 To<br/> |



 

## <a name="physical-memory-limits-windows-8"></a>Limites de la mémoire physique : Windows 8

Le tableau suivant spécifie les limites de la mémoire physique pour Windows 8.



| Version                | Limite sur x86    | Limite sur x64      |
|------------------------|-----------------|-------------------|
| Windows 8 Entreprise   | 4 Go<br/> | 512 Go<br/> |
| Windows 8 Professionnel | 4 Go<br/> | 512 Go<br/> |
| Windows 8              | 4 Go<br/> | 128 Go<br/> |



 

## <a name="physical-memory-limits-windows-server-2012"></a>Limites de la mémoire physique : Windows Server 2012

Le tableau suivant spécifie les limites de la mémoire physique pour Windows Server 2012. Windows Server 2012 n’est disponible que dans les éditions X64.



| Version                               | Limite sur x64     |
|---------------------------------------|------------------|
| Windows Server 2012 Datacenter        | 4 To<br/>  |
| Windows Server 2012 Standard          | 4 To<br/>  |
| Windows Server 2012 Essentials        | 64 Go<br/> |
| Windows Server 2012 Foundation        | 32 Go<br/> |
| Windows Storage Server 2012 Workgroup | 32 Go<br/> |
| Windows Storage Server 2012 Standard  | 4 To<br/>  |
| Hyper-V Server 2012                   | 4 To<br/>  |



 

## <a name="physical-memory-limits-windows-7"></a>limites de la mémoire physique : Windows 7

le tableau suivant spécifie les limites de la mémoire physique pour Windows 7.



| Version                | Limite sur x86    | Limite sur x64      |
|------------------------|-----------------|-------------------|
| Windows 7 Édition Intégrale     | 4 Go<br/> | 192 Go<br/> |
| Windows 7 Entreprise   | 4 Go<br/> | 192 Go<br/> |
| Windows 7 Professionnel | 4 Go<br/> | 192 Go<br/> |
| Windows 7 Édition Familiale Premium | 4 Go<br/> | 16 Go<br/>  |
| Windows 7 Édition Familiale Basique   | 4 Go<br/> | 8 Go<br/>   |
| Windows 7 Édition Starter      | 2 Go<br/> | N/A<br/>    |



 

## <a name="physical-memory-limits-windows-server-2008-r2"></a>limites de la mémoire physique : Windows Server 2008 R2

le tableau suivant spécifie les limites de la mémoire physique pour Windows Server 2008 R2. Windows Le serveur 2008 R2 est disponible uniquement dans les éditions 64 bits.



| Version                                          | Limite sur x64      | Limite sur IA64   |
|--------------------------------------------------|-------------------|-----------------|
| Windows Server 2008 R2 Datacenter                | 2 To<br/>   |                 |
| Windows Server 2008 R2 Entreprise                | 2 To<br/>   |                 |
| Windows Server 2008 R2 pour les systèmes Itanium |                   | 2 To<br/> |
| Windows Server 2008 R2 Foundation                | 8 Go<br/>   |                 |
| Windows Server 2008 R2 Standard                  | 32 Go<br/>  |                 |
| Windows HPC Server 2008 R2                       | 128 Go<br/> |                 |
| Windows Web Server 2008 R2                       | 32 Go<br/>  |                 |



 

## <a name="physical-memory-limits-windows-server-2008"></a>limites de la mémoire physique : Windows Server 2008

le tableau suivant spécifie les limites de la mémoire physique pour Windows Server 2008. les limites supérieures à 4 go pour 32 bits Windows supposent que [PAE](physical-address-extension.md) est activé.



| Version                                       | Limite sur x86     | Limite sur x64      | Limite sur IA64   |
|-----------------------------------------------|------------------|-------------------|-----------------|
| Windows Server 2008 Datacenter                | 64 Go<br/> | 1 To<br/>   |                 |
| Windows Server 2008 Entreprise                | 64 Go<br/> | 1 To<br/>   |                 |
| Windows Server 2008 HPC Edition               |                  | 128 Go<br/> |                 |
| Windows Server 2008 Standard                  | 4 Go<br/>  | 32 Go<br/>  |                 |
| Windows Server 2008 pour les systèmes Itanium |                  |                   | 2 To<br/> |
| Windows Small Business Server 2008            | 4 Go<br/>  | 32 Go<br/>  |                 |
| Windows Web Server 2008                       | 4 Go<br/>  | 32 Go<br/>  |                 |



 

## <a name="physical-memory-limits-windows-vista"></a>limites de la mémoire physique : Windows Vista

le tableau suivant spécifie les limites de la mémoire physique pour Windows Vista.



| Version                    | Limite sur x86    | Limite sur x64      |
|----------------------------|-----------------|-------------------|
| Windows Vista Édition Intégrale     | 4 Go<br/> | 128 Go<br/> |
| Windows Vista Entreprise   | 4 Go<br/> | 128 Go<br/> |
| Windows Vista Professionnel     | 4 Go<br/> | 128 Go<br/> |
| Windows Vista Édition Familiale Premium | 4 Go<br/> | 16 Go<br/>  |
| Windows Vista Édition Familiale Basique   | 4 Go<br/> | 8 Go<br/>   |
| Windows Vista Starter      | 1 Go<br/> |                   |



 

## <a name="physical-memory-limits-windows-home-server"></a>limites de la mémoire physique : Windows serveur d’hébergement

Windows Le serveur d’hébergement est disponible uniquement dans une édition 32 bits. La limite de la mémoire physique est de 4 Go.

## <a name="physical-memory-limits-windows-server-2003-r2"></a>limites de la mémoire physique : Windows Server 2003 R2

le tableau suivant spécifie les limites de la mémoire physique pour Windows Server 2003 R2. les limites supérieures à 4 go pour l’Windows 32 bits supposent que [PAE](physical-address-extension.md) est activé.



| Version                                              | Limite sur x86                                 | Limite sur x64     |
|------------------------------------------------------|----------------------------------------------|------------------|
| Windows Server 2003 R2 édition Datacenter<br/> | 64 Go<br/> (16 Go avec 4GT)<br/> | 1 To<br/>  |
| Windows Server 2003 R2 Enterprise Edition<br/> | 64 Go<br/> (16 Go avec 4GT)<br/> | 1 To<br/>  |
| Windows serveur 2003 R2 Édition Standard<br/>   | 4 Go<br/>                              | 32 Go<br/> |



 

## <a name="physical-memory-limits-windows-server-2003-with-service-pack-2-sp2"></a>limites de la mémoire physique : Windows Server 2003 avec Service Pack 2 (SP2)

le tableau suivant spécifie les limites de la mémoire physique pour Windows Server 2003 avec Service Pack 2 (SP2). les limites supérieures à 4 go pour l’Windows 32 bits supposent que [PAE](physical-address-extension.md) est activé.



| Version                                                                      | Limite sur x86                                 | Limite sur x64     | Limite sur IA64   |
|------------------------------------------------------------------------------|----------------------------------------------|------------------|-----------------|
| Windows Server 2003 avec Service Pack 2 (SP2), Datacenter Edition<br/> | 64 Go<br/> (16 Go avec 4GT)<br/> | 1 To<br/>  | 2 To<br/> |
| Windows Server 2003 avec Service Pack 2 (SP2), Êdition Entreprise<br/> | 64 Go<br/> (16 Go avec 4GT)<br/> | 1 To<br/>  | 2 To<br/> |
| Windows Server 2003 avec Service Pack 2 (SP2), Édition Standard<br/>   | 4 Go<br/>                              | 32 Go<br/> |                 |



 

## <a name="physical-memory-limits-windows-server-2003-with-service-pack-1-sp1"></a>limites de la mémoire physique : Windows Server 2003 avec Service Pack 1 (SP1)

le tableau suivant spécifie les limites de la mémoire physique pour Windows Server 2003 avec Service Pack 1 (SP1). les limites supérieures à 4 go pour l’Windows 32 bits supposent que [PAE](physical-address-extension.md) est activé.



| Version                                                                      | Limite sur x86                                 | Limite sur x64        | Limite sur IA64   |
|------------------------------------------------------------------------------|----------------------------------------------|---------------------|-----------------|
| Windows Server 2003 avec Service Pack 1 (SP1), Datacenter Edition<br/> | 64 Go<br/> (16 Go avec 4GT)<br/> | 1 TO X64<br/> | 1 To<br/> |
| Windows Server 2003 avec Service Pack 1 (SP1), Êdition Entreprise<br/> | 64 Go<br/> (16 Go avec 4GT)<br/> | 1 TO X64<br/> | 1 To<br/> |
| Windows Server 2003 avec Service Pack 1 (SP1), Édition Standard<br/>   | 4 Go<br/>                              | 32 Go<br/>    |                 |



 

## <a name="physical-memory-limits-windows-server-2003"></a>limites de la mémoire physique : Windows Server 2003

le tableau suivant spécifie les limites de la mémoire physique pour Windows Server 2003. les limites supérieures à 4 go pour l’Windows 32 bits supposent que [PAE](physical-address-extension.md) est activé.



| Version                                                    | Limite sur x86                                 | Limite sur IA64     |
|------------------------------------------------------------|----------------------------------------------|-------------------|
| Windows Server 2003 Datacenter Edition<br/>         | 64 Go<br/> (16 Go avec 4GT)<br/> | 512 Go<br/> |
| Windows Server 2003 Enterprise Edition<br/>         | 64 Go<br/> (16 Go avec 4GT)<br/> | 512 Go<br/> |
| Windows Server 2003 Standard Edition<br/>           | 4 Go<br/>                              |                   |
| Windows Server 2003, édition Web<br/>                | 2 Go<br/>                              |                   |
| Windows Small Business Server 2003<br/>              | 4 Go<br/>                              |                   |
| Windows Compute Cluster Server 2003<br/>             |                                              | 32 Go<br/>  |
| Windows Stockage Server 2003, Êdition Entreprise<br/> | 8 Go<br/>                              |                   |
| Windows Storage Server 2003<br/>                     | 4 Go<br/>                              |                   |



 

## <a name="physical-memory-limits-windows-xp"></a>limites de la mémoire physique : Windows XP

le tableau suivant spécifie les limites de la mémoire physique pour Windows XP.



| Version                    | Limite sur x86      | Limite sur x64      | Limite sur IA64                     |
|----------------------------|-------------------|-------------------|-----------------------------------|
| Windows XP                 | 4 Go<br/>   | 128 Go<br/> | 128 Go (non pris en charge)<br/> |
| Windows XP Starter Edition | 512 Mo<br/> | N/A<br/>    | N/A<br/>                    |



 

## <a name="physical-memory-limits-windows-embedded"></a>limites de la mémoire physique : Windows incorporée

le tableau suivant spécifie les limites de la mémoire physique pour Windows incorporée.



| Version                                   | Limite sur x86    | Limite sur x64      |
|-------------------------------------------|-----------------|-------------------|
| Windows XP Embedded<br/>            | 4 Go<br/> |                   |
| Windows Embedded Standard 2009<br/> | 4 Go<br/> |                   |
| Windows Embedded Standard 7<br/>    | 4 Go<br/> | 192 Go<br/> |



 

## <a name="how-graphics-cards-and-other-devices-affect-memory-limits"></a>Comment les cartes graphiques et les autres périphériques affectent les limites de mémoire

les appareils doivent mapper leur mémoire inférieure à 4 go pour des compatibilités avec les versions de Windows non compatibles PAE. Par conséquent, si le système dispose de 4 Go de RAM, certaines d’entre elles sont désactivées ou remappées au-delà de 4 Go par le BIOS. si la mémoire est remappée, les Windows X64 peuvent utiliser cette mémoire. les versions clientes X86 de Windows ne prennent pas en charge la mémoire physique au-delà de la marque de 4 go, afin qu’elles ne puissent pas accéder à ces régions remappées. toute version X64 Windows ou serveur X86 peut.

Les versions du client x86 avec PAE activé disposent d’un espace d’adressage physique 37 bits (128 Go) utilisable. Les limites imposées par ces versions sont l’adresse RAM physique maximale autorisée, et non la taille de l’espace d’e/s. Cela signifie que les pilotes compatibles PAE peuvent réellement utiliser l’espace physique au-delà de 4 Go s’ils le souhaitent. Par exemple, les pilotes peuvent mapper les régions de mémoire « perdues » situées au-dessus de 4 Go et exposer cette mémoire en tant que disque RAM.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Réglage à 4 gigaoctets](4-gigabyte-tuning.md)
</dt> <dt>

[**prise \_ en \_ \_ charge d’adresses volumineuses dans un fichier image \_**](/windows/win32/api/dbghelp/ns-dbghelp-loaded_image)
</dt> <dt>

[Extension d’adresse physique](physical-address-extension.md)
</dt> </dl>

 

 
