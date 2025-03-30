# Gestion de la Base de Données d'un Hôtel

## Contexte
Après la construction de ses hôtels dans une des zones touristiques, un directeur souhaite préparer une base de données pour faciliter la gestion de ses données.

Le directeur vous a présenté les informations suivantes à travers le modèle de relation entre entités :

![Modèle de Relation Entre Entités](https://i.imgur.com/oHkrfiJ.png)

## Instructions
Convertir le modèle de relations entre entités en un diagramme relationnel.

## Solution
Voici la transformation du modèle de relation entre entités en un schéma relationnel :

### Tables et leurs attributs

#### **Hotel**
- `Hotel_Id` (Primary Key)
- `Hotel_Name`

#### **Type**
- `Type_Id` (Primary Key)
- `Type_Name`

#### **Room**
- `Room_Id` (Primary Key)
- `Floor`
- `Hotel_Id` (Foreign Key référant `Hotel`)
- `Type_Id` (Foreign Key référant `Type`)

#### **Category**
- `Category_Id` (Primary Key)
- `Category_Name`
- `Price`
- `Beds_Numbers`

#### **Employee**
- `Employee_Id` (Primary Key)
- `Employee_Name`
- `Employee_Speciality`

### Relations entre les tables

#### **Works** (Relation entre `Employee` et `Hotel`)
- `Employee_Id` (Foreign Key référant `Employee`)
- `Hotel_Id` (Foreign Key référant `Hotel`)

#### **Leads** (Auto-relation `Employee`)
- `Leader_Id` (Foreign Key référant `Employee`)
- `Employee_Id` (Foreign Key référant `Employee`)

#### **Room_Category** (Relation entre `Room` et `Category`)
- `Room_Id` (Foreign Key référant `Room`)
- `Category_Id` (Foreign Key référant `Category`)

---

Ce fichier README sert de référence pour comprendre la structure de la base de données et son schéma relationnel.